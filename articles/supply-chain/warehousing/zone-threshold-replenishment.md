---
title: Áfyllingarmörk svæðis
description: Áfyllingarmörk svæðis notar lágmarks-/hámarkáfyllingarstefnu (lágm./hám.), en hún metur heil svæði í vöruhúsi í staðinn fyrir einstakar staðsetningar. Þar af leiðandi geta stjórnendur vöruhúsa skjótt komist að því þegar frekari birgða er krafist á tiltektarsvæði.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2e83d6885bf7400916d633a49d3b19b8843b0269
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965503"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="8d111-104">Áfyllingarmörk svæðis</span><span class="sxs-lookup"><span data-stu-id="8d111-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d111-105">Áfyllingarmörk svæðis notar [lágmarks-/hámarkáfyllingarstefnu](replenishment.md) (lágm./hám.), en hún metur heil svæði í vöruhúsi í staðinn fyrir einstakar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="8d111-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="8d111-106">Þar af leiðandi geta stjórnendur vöruhúsa skjótt komist að því þegar frekari birgða er krafist á tiltektarsvæði.</span><span class="sxs-lookup"><span data-stu-id="8d111-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="8d111-107">Uppsetningin fyrir þennan eiginleika líkist uppsetningunni fyrir áfyllingu miðað við staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="8d111-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="8d111-108">Hins vegar þegar þú setur upp sniðmát fyrir lágm./hám. áfyllingu geturðu einnig tilgreint hvort meta skal viðmiðunarmörkin fyrir hverja staðsetningu eða hvert svæði.</span><span class="sxs-lookup"><span data-stu-id="8d111-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="8d111-109">Ef þú setur upp mat sem byggir á svæðum verður þú að bæta við sérstökum svæðum við fyrirspurn vals á svæði.</span><span class="sxs-lookup"><span data-stu-id="8d111-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="8d111-110">Líkt og lágm./hám. áfyllingar sem miðast við staðsetningar, miðast lágm./hám. áfylling miðað við svæði á lágmarksviðmiðunarmörk birgðar sem kallar fram áfyllingarvinnu fyrir valdar vörur.</span><span class="sxs-lookup"><span data-stu-id="8d111-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="8d111-111">Þessi áfyllingarvinna eykur birgðir að tilgreindum hámarksviðmiðunarmörkum fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="8d111-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="8d111-112">Áfyllingarferli svæða fyrir afurðarafbrigði eru ekki studd í núverandi útgáfu.</span><span class="sxs-lookup"><span data-stu-id="8d111-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="8d111-113">Ólíkt lágm./hám. áfyllingu miðað við staðsetningar, krefst lágm./hám. áfylling sem miðast við svæði ekki fastra staðsetninga til að meta hvort staðsetningar ættu að geyma tiltekna vöru.</span><span class="sxs-lookup"><span data-stu-id="8d111-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="8d111-114">Þess vegna gerir áfylling sem miðast við svæði kleift að nota lágm./hám. áfyllingu jafnvel þó að þú hafir ekki fasta staðsetningu fyrir hverja vöru eða afurðarafbrigði í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="8d111-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="8d111-115">Þegar magn á svæðinu fellur undir tilgreind lágmarksviðmiðunarmörk verður til áfyllingarvinna.</span><span class="sxs-lookup"><span data-stu-id="8d111-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="8d111-116">Staðsetningarleiðbeiningar ákvarða staðsetninguna sem birgðunum er komið fyrir.</span><span class="sxs-lookup"><span data-stu-id="8d111-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="8d111-117">Kveikja á eiginleikanum áfyllingarmörk svæðis</span><span class="sxs-lookup"><span data-stu-id="8d111-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="8d111-118">Áður en þú getur notað eiginleikann *Áfyllingarmörk svæðis*, verður að vera kveikt á því í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="8d111-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="8d111-119">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="8d111-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="8d111-120">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="8d111-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8d111-121">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="8d111-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="8d111-122">**Heiti eiginleika:** *Áfyllingarmörk svæðis*</span><span class="sxs-lookup"><span data-stu-id="8d111-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="8d111-123">Uppsetning á áfyllingu miðað við svæði</span><span class="sxs-lookup"><span data-stu-id="8d111-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="8d111-124">Til að setja upp áfyllingu miðað við svæði verður þú að grunnstilla nokkra hluta kerfisins.</span><span class="sxs-lookup"><span data-stu-id="8d111-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="8d111-125">Þessi hluti kynnir ýmsar stillingar og gildi sýnigagna sem þú getur slegið inn ef þú vilt vinna í gegnum aðstæðurnar í lok þessa efnisatriðis.</span><span class="sxs-lookup"><span data-stu-id="8d111-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="8d111-126">Setja upp leiðbeiningarkóða</span><span class="sxs-lookup"><span data-stu-id="8d111-126">Set up directive codes</span></span>

<span data-ttu-id="8d111-127">[Leiðbeiningarkóðar](control-warehouse-location-directives.md) gera þér kleift að vera nákvæmari þegar þú skilgreinir staðsetningarsniðmáts sem er notað í vinnusniðmáti.</span><span class="sxs-lookup"><span data-stu-id="8d111-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="8d111-128">Hver kóði setur upp sameiginlegt gildi sem þú getur vísað til þegar þú grunnstillir hverja tegund sniðmáts fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="8d111-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="8d111-129">Skoða og breyta leiðbeiningarkóðum</span><span class="sxs-lookup"><span data-stu-id="8d111-129">View and edit directive codes</span></span>

<span data-ttu-id="8d111-130">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Leiðbeiningarkóðar** til að skoða eða breyta leiðbeiningarkóðunum.</span><span class="sxs-lookup"><span data-stu-id="8d111-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="8d111-131">Búa til leiðbeiningarkóða sýnigagna</span><span class="sxs-lookup"><span data-stu-id="8d111-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="8d111-132">Þetta dæmi sýnir hvernig á að búa til leiðbeiningarkóða.</span><span class="sxs-lookup"><span data-stu-id="8d111-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="8d111-133">Ef þú ætlar að vinna í gegnum aðstæðurnar í lok þessa efnisatriðis getur þú notað sýnigögnin sem koma fram hér.</span><span class="sxs-lookup"><span data-stu-id="8d111-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="8d111-134">Annars skaltu nota þín eigin gildi.</span><span class="sxs-lookup"><span data-stu-id="8d111-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="8d111-135">Veldu **USMF**-lögaðilann til að vinna með sýnigögnin.</span><span class="sxs-lookup"><span data-stu-id="8d111-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="8d111-136">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Leiðbeiningarkóðar**.</span><span class="sxs-lookup"><span data-stu-id="8d111-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="8d111-137">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="8d111-138">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="8d111-139">**Leiðbeiningarkóði:** _Áfylling svæða_</span><span class="sxs-lookup"><span data-stu-id="8d111-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="8d111-140">**Lýsing leiðbeininga:** _Áfylling svæða_</span><span class="sxs-lookup"><span data-stu-id="8d111-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="8d111-141">Veljið **Vista** til að vista nýja kóðann.</span><span class="sxs-lookup"><span data-stu-id="8d111-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="8d111-142">Setja upp sniðmát áfyllingar</span><span class="sxs-lookup"><span data-stu-id="8d111-142">Set up replenishment templates</span></span>

<span data-ttu-id="8d111-143">[Sniðmát fyrir lágm./hám. áfyllingar](tasks/set-up-min-max-replenishment-process.md) er aðalverkfærið til að viðhalda ákjósanlegum gildum á tiltektarstaðsetningum.</span><span class="sxs-lookup"><span data-stu-id="8d111-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="8d111-144">Í þessum sniðmátum verður þú að setja upp reglurnar sem verða notaðar til að fylla á birgðir í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="8d111-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="8d111-145">Áfyllingin sem hægt er að nota sniðmátin fyrir inniheldur áfyllingu miðað við svæði.</span><span class="sxs-lookup"><span data-stu-id="8d111-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="8d111-146">Skoða og breyta áfyllingarsniðmátum</span><span class="sxs-lookup"><span data-stu-id="8d111-146">View and edit replenishment templates</span></span>

<span data-ttu-id="8d111-147">Áfyllingarsniðmát er safn reglna sem stjórna því hvernig og hvenær fyllt er á staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="8d111-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="8d111-148">Þú velur sniðmát til að stjórna hvenær og hvernig áfylling á sér stað.</span><span class="sxs-lookup"><span data-stu-id="8d111-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="8d111-149">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Áfyllingarsniðmát** til að skoða eða breyta áfyllingarsniðmátum.</span><span class="sxs-lookup"><span data-stu-id="8d111-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="8d111-150">Undirbúningur áfyllingarsniðmáts með sýnigögnum</span><span class="sxs-lookup"><span data-stu-id="8d111-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="8d111-151">Þetta dæmi sýnir hvernig á að undirbúa áfyllingarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="8d111-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="8d111-152">Ef þú ætlar að vinna í gegnum aðstæðurnar í lok þessa efnisatriðis getur þú notað sýnigögnin sem koma fram hér.</span><span class="sxs-lookup"><span data-stu-id="8d111-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="8d111-153">Annars skaltu nota þín eigin gildi.</span><span class="sxs-lookup"><span data-stu-id="8d111-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="8d111-154">Veldu **USMF**-lögaðilann til að vinna með sýnigögnin.</span><span class="sxs-lookup"><span data-stu-id="8d111-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="8d111-155">Fara í **Vöruhúsakerfi \> Uppsetningu \> Áfylling \> Áfyllingarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="8d111-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="8d111-156">Veldu **Breyta** til að setja síðuna í breytingastillingu.</span><span class="sxs-lookup"><span data-stu-id="8d111-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="8d111-157">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="8d111-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="8d111-158">Í nýju línunni skal stilla eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="8d111-158">In the new row, set the following values.</span></span> <span data-ttu-id="8d111-159">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="8d111-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="8d111-160">**Áfyllingarsniðmát:** _Lágm./hám. áfylling fyrir svæði_</span><span class="sxs-lookup"><span data-stu-id="8d111-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="8d111-161">**Lýsing:** _Lágm./hám. áfylling_</span><span class="sxs-lookup"><span data-stu-id="8d111-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="8d111-162">**Gerð áfyllingar:** _Lágmarks eða hámarks_</span><span class="sxs-lookup"><span data-stu-id="8d111-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="8d111-163">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="8d111-163">Select **Save**.</span></span>
1. <span data-ttu-id="8d111-164">Þó að nýja línan sé enn valin í hnitanetinu **Yfirlit** skaltu velja **Nýtt** fyrir ofan hnitanetið **Upplýsingar um áfyllingarsniðmát** til að bæta við línu sem er tengd við áfyllingarsniðmátið *Lágm./hám. áfylling fyrir svæði* sem þú varst að búa til.</span><span class="sxs-lookup"><span data-stu-id="8d111-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="8d111-165">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="8d111-166">**Raðnúmer:** Sláðu inn _1_.</span><span class="sxs-lookup"><span data-stu-id="8d111-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="8d111-167">**Lýsing** Sláðu inn _Áfylling tiltektarsvæðis_.</span><span class="sxs-lookup"><span data-stu-id="8d111-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="8d111-168">**Áfyllingareining** Veldu _ea_.</span><span class="sxs-lookup"><span data-stu-id="8d111-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="8d111-169">**Tegund beiðni::** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="8d111-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="8d111-170">**Staðsetningarleiðbeiningar:** Þetta svæði tengir áfyllingarsniðmátið við staðsetningarleiðbeiningarnar.</span><span class="sxs-lookup"><span data-stu-id="8d111-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="8d111-171">Veldu staðsetningakóða sýnigagnanna sem þú bjóst til áður (_Áfylling fyrir svæði_).</span><span class="sxs-lookup"><span data-stu-id="8d111-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="8d111-172">**Vinnusniðmát:** Skildu þetta svæði eftir autt.</span><span class="sxs-lookup"><span data-stu-id="8d111-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="8d111-173">**Lágmarksmagn:** Þetta svæði setur upp magnið sem áfylling verður sett af stað.</span><span class="sxs-lookup"><span data-stu-id="8d111-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="8d111-174">Færðu inn _50_.</span><span class="sxs-lookup"><span data-stu-id="8d111-174">Enter _50_.</span></span>
    - <span data-ttu-id="8d111-175">**Hámarksmagn:** Þetta svæði stillir hámarksmagn vöru sem getur verið til staðar á svæði.</span><span class="sxs-lookup"><span data-stu-id="8d111-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="8d111-176">Framleidd áfyllingarvinna eykur birgðirnar um þetta magn.</span><span class="sxs-lookup"><span data-stu-id="8d111-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="8d111-177">Færðu inn _150_.</span><span class="sxs-lookup"><span data-stu-id="8d111-177">Enter _150_.</span></span>
    - <span data-ttu-id="8d111-178">**Eining:** Þetta svæði úthluta einingu fyrir lágmarks- og hámarksgildi.</span><span class="sxs-lookup"><span data-stu-id="8d111-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="8d111-179">Veldu _ea_.</span><span class="sxs-lookup"><span data-stu-id="8d111-179">Select _ea_.</span></span>
    - <span data-ttu-id="8d111-180">**Aukning eftirspurnar:** Veldu _Námunda_.</span><span class="sxs-lookup"><span data-stu-id="8d111-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="8d111-181">**Fylla á auðar fastar staðsetningar:** Merktu í þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="8d111-182">**Fylla aðeins á fastar staðsetningar:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-183">**Fyrirspurnarstilling afurðar:** Veldu _Fyrirspurn afurðar_.</span><span class="sxs-lookup"><span data-stu-id="8d111-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="8d111-184">**Viðmiðunarmörk áfyllingar:**: Þetta svæði skilgreinir hvort sniðmátið eigi að meta eftir svæði eða eftir tiltekinni staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="8d111-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="8d111-185">Veldu _Svæði_.</span><span class="sxs-lookup"><span data-stu-id="8d111-185">Select _Zone_.</span></span>
    - <span data-ttu-id="8d111-186">**Vöruhús:** veldu _61_.</span><span class="sxs-lookup"><span data-stu-id="8d111-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="8d111-187">Veldu **Velja afurðir** fyrir ofan hnitanetið **Upplýsingar um áfyllingarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="8d111-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="8d111-188">Í svarglugga **Fyrirspurn afurðar** á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="8d111-189">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="8d111-190">**Tafla:** _Vara_</span><span class="sxs-lookup"><span data-stu-id="8d111-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="8d111-191">**Afleidd tafla:** _Vara_</span><span class="sxs-lookup"><span data-stu-id="8d111-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="8d111-192">**Svæði:** _Vörunúmer_</span><span class="sxs-lookup"><span data-stu-id="8d111-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="8d111-193">**Skilyrði:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="8d111-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="8d111-194">Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="8d111-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="8d111-195">Veldu **Svæði til að fylla á** fyrir ofan hnitanetið **Upplýsingar um áfyllingarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="8d111-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="8d111-196">Í svarglugga **Fyrirspurn afurðar** á flipanum **Svið** bætir þú línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="8d111-197">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="8d111-198">**Tafla:** _Svæði í vöruhúsi_</span><span class="sxs-lookup"><span data-stu-id="8d111-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="8d111-199">**Afleidd tafla:** _Svæði í vöruhúsi_</span><span class="sxs-lookup"><span data-stu-id="8d111-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="8d111-200">**Reitur::** _Auðkenni svæðis_</span><span class="sxs-lookup"><span data-stu-id="8d111-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="8d111-201">**Skilyrði:** _GÓLF_</span><span class="sxs-lookup"><span data-stu-id="8d111-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="8d111-202">Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="8d111-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="8d111-203">Setja upp staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="8d111-203">Set up location directives</span></span>

<span data-ttu-id="8d111-204">Ólíkt lágm./hám. áfyllingu miðað við staðsetningu, krefst lágm./hám. áfylling miðað við svæði þess að þú setjir bæði upp staðsetningarleiðbeiningar og leiðbeiningar fyrir frágangsstaðsetningar, vegna þess að kerfið metur allt svæðið í staðinn fyrir að tiltektarstaðsetninguna fyrir vinnu á útleið.</span><span class="sxs-lookup"><span data-stu-id="8d111-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="8d111-205">Skoða og breyta staðsetningarleiðbeiningum</span><span class="sxs-lookup"><span data-stu-id="8d111-205">View and edit location directives</span></span>

<span data-ttu-id="8d111-206">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar** til að skoða eða breyta staðsetningarleiðbeiningunum þínum.</span><span class="sxs-lookup"><span data-stu-id="8d111-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="8d111-207">Fyrir dæmi sem sýna hvernig nota á stillingarnar til að búa til áskildar leiðbeiningar fyrir tiltektarstaðsetningar og leiðbeiningar fyrir frágangsstaðsetningar, sjá næsta kafla.</span><span class="sxs-lookup"><span data-stu-id="8d111-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="8d111-208">Undirbúningur staðsetningarleiðbeininga úr sýnigögnum</span><span class="sxs-lookup"><span data-stu-id="8d111-208">Prepare demo data location directives</span></span>

<span data-ttu-id="8d111-209">Til að útbúa sýnigögn svo hægt sé að nota þau við aðstæðurnar í lok þessa efnisatriðis, verður þú að búa til tvær staðsetningarleiðbeiningar: eina fyrir tiltekt og eina fyrir frágang.</span><span class="sxs-lookup"><span data-stu-id="8d111-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="8d111-210">Búa til leiðbeiningar um tiltekt áfyllingar</span><span class="sxs-lookup"><span data-stu-id="8d111-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="8d111-211">Veldu **USMF**-lögaðilann til að vinna með sýnigögnin.</span><span class="sxs-lookup"><span data-stu-id="8d111-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="8d111-212">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="8d111-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="8d111-213">Stilltu svæðið **Gerð verkbeiðni** á _Áfylling_ í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="8d111-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="8d111-214">Veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjar leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="8d111-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="8d111-215">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-215">Set the following values:</span></span>

    - <span data-ttu-id="8d111-216">**Raðnúmer:** Samþykkja sjálfgildið.</span><span class="sxs-lookup"><span data-stu-id="8d111-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="8d111-217">**Heiti:** Sláðu inn _Tiltekt á svæði_.</span><span class="sxs-lookup"><span data-stu-id="8d111-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="8d111-218">**Tegund vinnu:** Veldu _Tiltekt_.</span><span class="sxs-lookup"><span data-stu-id="8d111-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="8d111-219">**Svæði:** Veldu _6_.</span><span class="sxs-lookup"><span data-stu-id="8d111-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="8d111-220">**Vöruhús:** veldu _61_.</span><span class="sxs-lookup"><span data-stu-id="8d111-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="8d111-221">**Leiðbeiningarkóði:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="8d111-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="8d111-222">**Margar birgðahaldseiningar:** Stilltu þennan möguleika á _Nei_.</span><span class="sxs-lookup"><span data-stu-id="8d111-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="8d111-223">Veldu **Vista** til að búa til leiðbeiningar sem hafa stillingarnar sem þú hefur grunnstillt hingað til.</span><span class="sxs-lookup"><span data-stu-id="8d111-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="8d111-224">Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="8d111-225">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="8d111-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="8d111-226">**Raðnúmer:** Sláðu inn _1_.</span><span class="sxs-lookup"><span data-stu-id="8d111-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="8d111-227">**Frá-magn:** Sláðu inn _0_.</span><span class="sxs-lookup"><span data-stu-id="8d111-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="8d111-228">**Til-magn** Enter _10000000_.</span><span class="sxs-lookup"><span data-stu-id="8d111-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="8d111-229">**Eining:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="8d111-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="8d111-230">**Finna magn:** Veldu _Ekkert_.</span><span class="sxs-lookup"><span data-stu-id="8d111-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="8d111-231">**Takmarka eftir einingu:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-232">**Námunda eftir einingu:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-233">**Finna umbúðarmagn:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-234">**Leyfa að skipta:** Hakið í þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="8d111-235">Veljið **Vista** til að vista nýju línuna.</span><span class="sxs-lookup"><span data-stu-id="8d111-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="8d111-236">Þó að nýja línan þín sé enn valin á hnitanetinu **Línur** skaltu velja **Nýtt** á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="8d111-237">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="8d111-238">**Raðnúmer:** Sláðu inn _1_.</span><span class="sxs-lookup"><span data-stu-id="8d111-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="8d111-239">**Heiti:** Sláðu inn _Tiltekt úr lausu_.</span><span class="sxs-lookup"><span data-stu-id="8d111-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="8d111-240">**Notkun fastrar staðsetningar:** Veldu _Fastar og lausar staðsetningar_.</span><span class="sxs-lookup"><span data-stu-id="8d111-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="8d111-241">**Leyfa neikvæðar birgðir:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-242">**Runa virk:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-243">**Áætlun:** Veldu _Engin_.</span><span class="sxs-lookup"><span data-stu-id="8d111-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="8d111-244">Veljið **Vista** til að vista nýju aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="8d111-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="8d111-245">Þó að nýja aðgerðin þín sé enn valin skaltu velja **Breyta fyrirspurn** fyrir ofan hnitanetið **Aðgerðir í staðsetningarleiðbeiningum**.</span><span class="sxs-lookup"><span data-stu-id="8d111-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="8d111-246">Svargluggi fyrirspurnar birtist þar sem þú getur valið staðsetningarnar sem skal fylla á úr.</span><span class="sxs-lookup"><span data-stu-id="8d111-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="8d111-247">Veldu **Bæta við** til að bæta við röð á flipanum **Svið** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="8d111-248">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="8d111-249">**Tafla:** _Staðir_</span><span class="sxs-lookup"><span data-stu-id="8d111-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="8d111-250">**Afleidd tafla:** _Staðsetningar_</span><span class="sxs-lookup"><span data-stu-id="8d111-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="8d111-251">**Reitur::** _Auðkenni svæðis_</span><span class="sxs-lookup"><span data-stu-id="8d111-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="8d111-252">**Skilyrði:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="8d111-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="8d111-253">Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="8d111-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="8d111-254">Smelltu á **Vista** til að vista staðsetningarleiðbeiningarnar þínar.</span><span class="sxs-lookup"><span data-stu-id="8d111-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="8d111-255">Búa til leiðbeiningar um frátekt áfyllingar</span><span class="sxs-lookup"><span data-stu-id="8d111-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="8d111-256">Á síðunni **Staðsetningarleiðbeiningar** í vinstri glugganum skaltu ganga úr skugga um að svæðið **Gerð verkbeiðni** sé enn stilltur á _Áfyllingu_.</span><span class="sxs-lookup"><span data-stu-id="8d111-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="8d111-257">Veldu **Nýtt** á aðgerðasvæðinu til að búa til aðrar nýjar leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="8d111-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="8d111-258">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-258">Set the following values:</span></span>

    - <span data-ttu-id="8d111-259">**Raðnúmer:** Samþykkja sjálfgildið.</span><span class="sxs-lookup"><span data-stu-id="8d111-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="8d111-260">**Heiti:** Sláðu inn _Frágangur á svæði_.</span><span class="sxs-lookup"><span data-stu-id="8d111-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="8d111-261">**Gerð verkbeiðni:** Veldu _Frágangur_.</span><span class="sxs-lookup"><span data-stu-id="8d111-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="8d111-262">**Svæði:** Veldu _6_.</span><span class="sxs-lookup"><span data-stu-id="8d111-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="8d111-263">**Vöruhús:** veldu _61_.</span><span class="sxs-lookup"><span data-stu-id="8d111-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="8d111-264">**Leiðbeiningarkóði:** Veldu _Áfylling á svæði_ til að tengja þessar staðsetningarleiðbeiningar við áfyllingarsniðmátið sem þú bjóst til áður með því að nota kóðann sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="8d111-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="8d111-265">**Margar birgðahaldseiningar:** Stilltu þennan möguleika á _Nei_.</span><span class="sxs-lookup"><span data-stu-id="8d111-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="8d111-266">Veldu **Vista** til að búa til leiðbeiningar sem hafa stillingarnar sem þú hefur grunnstillt hingað til.</span><span class="sxs-lookup"><span data-stu-id="8d111-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="8d111-267">Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="8d111-268">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="8d111-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="8d111-269">**Raðnúmer:** Sláðu inn _1_.</span><span class="sxs-lookup"><span data-stu-id="8d111-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="8d111-270">**Frá-magn:** Sláðu inn _0_.</span><span class="sxs-lookup"><span data-stu-id="8d111-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="8d111-271">**Til-magn** Enter _10000000_.</span><span class="sxs-lookup"><span data-stu-id="8d111-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="8d111-272">**Eining:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="8d111-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="8d111-273">**Finna magn:** Veldu _Ekkert_.</span><span class="sxs-lookup"><span data-stu-id="8d111-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="8d111-274">**Takmarka eftir einingu:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-275">**Námunda eftir einingu:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-276">**Finna umbúðarmagn:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-277">**Leyfa að skipta:** Hakið í þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="8d111-278">Veljið **Vista** til að vista nýju línuna.</span><span class="sxs-lookup"><span data-stu-id="8d111-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="8d111-279">Þó að nýja línan þín sé enn valin á hnitanetinu **Línur** skaltu velja **Nýtt** á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="8d111-280">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="8d111-281">**Raðnúmer:** Sláðu inn _1_.</span><span class="sxs-lookup"><span data-stu-id="8d111-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="8d111-282">**Heiti:** Sláðu inn _Frágangur á svæði_.</span><span class="sxs-lookup"><span data-stu-id="8d111-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="8d111-283">**Notkun fastrar staðsetningar:** Veldu _Fastar og lausar staðsetningar_.</span><span class="sxs-lookup"><span data-stu-id="8d111-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="8d111-284">**Leyfa neikvæðar birgðir:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-285">**Runa virk:** Hreinsaðu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="8d111-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="8d111-286">**Áætlun:** Veldu _Sameina_.</span><span class="sxs-lookup"><span data-stu-id="8d111-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="8d111-287">Veljið **Vista** til að vista nýju aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="8d111-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="8d111-288">Veldu nýju aðgerðina þína og veldu **Breyta fyrirspurn** fyrir ofan hnitanetið **Aðgerðir í staðsetningarleiðbeiningum**.</span><span class="sxs-lookup"><span data-stu-id="8d111-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="8d111-289">Svargluggi fyrirspurnar birtist þar sem þú getur valið svæðið sem á að fylla á.</span><span class="sxs-lookup"><span data-stu-id="8d111-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="8d111-290">Þetta svæði ætti að vera sama svæði og er tilgreint í áfyllingarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="8d111-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="8d111-291">Veldu **Bæta við** til að bæta við röð á flipanum **Svið** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="8d111-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="8d111-292">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="8d111-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="8d111-293">**Tafla:** _Staðir_</span><span class="sxs-lookup"><span data-stu-id="8d111-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="8d111-294">**Afleidd tafla:** _Staðsetningar_</span><span class="sxs-lookup"><span data-stu-id="8d111-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="8d111-295">**Reitur::** _Auðkenni svæðis_</span><span class="sxs-lookup"><span data-stu-id="8d111-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="8d111-296">**Skilyrði:** _GÓLF_</span><span class="sxs-lookup"><span data-stu-id="8d111-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="8d111-297">Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="8d111-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="8d111-298">Smelltu á **Vista** til að vista staðsetningarleiðbeiningarnar þínar.</span><span class="sxs-lookup"><span data-stu-id="8d111-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="8d111-299">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="8d111-299">Scenario</span></span>

<span data-ttu-id="8d111-300">Þessi hluti fjallar um sýniaðstæður sem sýna hvernig á að vinna með eiginleikann.</span><span class="sxs-lookup"><span data-stu-id="8d111-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="8d111-301">Undirbúið áskilin sýnigögn fyrir sýniaðstæðurnar</span><span class="sxs-lookup"><span data-stu-id="8d111-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="8d111-302">Áður en byrjað er að vinna í gegnum aðstæðurnar verður þú að virkja sýnigögn og setja upp eiginleikann eins og lýst er í þessum kafla og fyrri köflum í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="8d111-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="8d111-303">Nota USMF-lögaðilann</span><span class="sxs-lookup"><span data-stu-id="8d111-303">Use the USMF legal entity</span></span>

<span data-ttu-id="8d111-304">Til að vinna í gegnum aðstæðurnar með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="8d111-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="8d111-305">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="8d111-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="8d111-306">Undirbúningur viðbótarsýnigagna</span><span class="sxs-lookup"><span data-stu-id="8d111-306">Prepare additional sample data</span></span>

<span data-ttu-id="8d111-307">Eftir að þú hefur valið **USMF**-lögaðilann skaltu bæta við viðbótarsýnigögnum sem krafist er, eins og lýst er í hlutanum [Uppsetning á áfyllingu miðað við svæði](#setup) fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="8d111-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="8d111-308">Athuga lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="8d111-308">Check your on-hand inventory</span></span>

<span data-ttu-id="8d111-309">Fylgdu þessum skrefum til að ganga úr skugga um að kerfið þitt sé með nægar birgðir til að styðja sýniaðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="8d111-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="8d111-310">Gakktu úr skugga um að lagerbirgðir séu til staðar fyrir vöruna *A0001* á tveimur mismunandi staðsetningum á tiltektarsvæðinu (*GÓLFI*) sem er tilgreint í áfyllingarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="8d111-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="8d111-311">Samt sem áður ættu heildarbirgðirnar að vera minni en áskilið lágmarksmagn (*50*) sem er tilgreint í áfyllingarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="8d111-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="8d111-312">Á þennan hátt er hægt að líkja eftir því hvernig útreikningur á sér stað fyrir allt svæðið í stað einnar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="8d111-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="8d111-313">**Notaðu hvaða vöruhúsaferli sem er til að breyta birgðunum eftir þörfum.**</span><span class="sxs-lookup"><span data-stu-id="8d111-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="8d111-314">Gakktu úr skugga um að nægar birgðir séu fyrir vöru *A0001* á fjöldastaðsetningu sem er tilgreint í staðsetningarleiðbeiningu tiltektar á svæði þar sem áfyllingarvinnan skal taka til vörur á svæðisauðkenni *MAGN*.</span><span class="sxs-lookup"><span data-stu-id="8d111-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="8d111-315">Heildarbirgðir verða að vera meiri en áskilið hámarksmagn (*150*) sem er tilgreint í áfyllingarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="8d111-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="8d111-316">Valfrjálst en ráðlagt: Fylgdu eftirfarandi skrefum til að búa til leiðréttingabók birgða:</span><span class="sxs-lookup"><span data-stu-id="8d111-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="8d111-317">Farið í **Birgðastjórnun \> Færslubókarfærslur \> Vörur \> Leiðrétting birgða**.</span><span class="sxs-lookup"><span data-stu-id="8d111-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="8d111-318">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8d111-318">Select **New**.</span></span>
    1. <span data-ttu-id="8d111-319">Í svarglugganum **Stofna birgðabók** á svæðinu **Vöruhús** velur þú *61*.</span><span class="sxs-lookup"><span data-stu-id="8d111-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="8d111-320">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8d111-320">Select **OK**.</span></span>
    1. <span data-ttu-id="8d111-321">Á flýtiflipanum **Færslubókarlínur** notar þú hnappinn **Ný** til að bæta við þremur línum við töfluna og stilla eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="8d111-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="8d111-322">Eftir að þú hefur lokið við að setja upp hverja línu skaltu velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="8d111-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="8d111-323">**Lína 1:**</span><span class="sxs-lookup"><span data-stu-id="8d111-323">**Line 1:**</span></span>

            - <span data-ttu-id="8d111-324">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8d111-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="8d111-325">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="8d111-325">**Site:** *6*</span></span>
            - <span data-ttu-id="8d111-326">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="8d111-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="8d111-327">**Staðsetning:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="8d111-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="8d111-328">**Númeraplata:** Veldu fyrirliggjandi númeraplötu á listanum eða búðu til nýja númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="8d111-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="8d111-329">**Magn:** *1000*</span><span class="sxs-lookup"><span data-stu-id="8d111-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="8d111-330">**Lína 2:**</span><span class="sxs-lookup"><span data-stu-id="8d111-330">**Line 2:**</span></span>

            - <span data-ttu-id="8d111-331">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8d111-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="8d111-332">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="8d111-332">**Site:** *6*</span></span>
            - <span data-ttu-id="8d111-333">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="8d111-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="8d111-334">**Staðsetning:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="8d111-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="8d111-335">**Númeraplata:** Veldu fyrirliggjandi númeraplötu á listanum eða búðu til nýja númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="8d111-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="8d111-336">**Magn:** *15*</span><span class="sxs-lookup"><span data-stu-id="8d111-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="8d111-337">**Lína 3:**</span><span class="sxs-lookup"><span data-stu-id="8d111-337">**Line 3:**</span></span>

            - <span data-ttu-id="8d111-338">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8d111-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="8d111-339">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="8d111-339">**Site:** *6*</span></span>
            - <span data-ttu-id="8d111-340">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="8d111-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="8d111-341">**Staðsetning:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="8d111-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="8d111-342">**Númeraplata:** Veldu fyrirliggjandi númeraplötu á listanum eða búðu til nýja númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="8d111-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="8d111-343">**Magn:** *10*</span><span class="sxs-lookup"><span data-stu-id="8d111-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="8d111-344">Veldu **Villuleita** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="8d111-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="8d111-345">Leiðréttu allar villur sem koma í ljós áður en þú ferð í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="8d111-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="8d111-346">Veldu **Bóka** á aðgerðarsvæðinu til að bóka birgðir í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="8d111-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="8d111-347">Sýniaðstæður: Keyra lágm./hám. áfyllingu miðað við svæði</span><span class="sxs-lookup"><span data-stu-id="8d111-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="8d111-348">Þegar öll áskilin sýnigögn eru til staðar, getur þú hrint af stað áfyllingu með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8d111-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="8d111-349">Fara í **Vöruhúsakerfi \> Áfylling \> Áfyllingar**.</span><span class="sxs-lookup"><span data-stu-id="8d111-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="8d111-350">Í svarglugganum **Áfylling** á flýtiflipanum **Færslur sem á að taka með** velur þú **Sía**.</span><span class="sxs-lookup"><span data-stu-id="8d111-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="8d111-351">Í svarglugganum **Fyrirspurn** á flipanum **Svið** breytir þú sjálfgefnu töflulínunni á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="8d111-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="8d111-352">**Tafla:** Veldu _Áfyllingarsniðmát_.</span><span class="sxs-lookup"><span data-stu-id="8d111-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="8d111-353">**Afleidd tafla:** Veldu _Áfyllingarsniðmát_.</span><span class="sxs-lookup"><span data-stu-id="8d111-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="8d111-354">**Svæði:** Veldu _Áfyllingarsniðmát_.</span><span class="sxs-lookup"><span data-stu-id="8d111-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="8d111-355">**Skilyrði:** Veldu _Lágm./hám. áfylling á svæði_.</span><span class="sxs-lookup"><span data-stu-id="8d111-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="8d111-356">Þetta áfyllingarsniðmát er áfyllingarsniðmátið sem þú bjóst til meðan þú varst að undirbúa sýnigögnin fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="8d111-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="8d111-357">Veldu **Í lagi** til að vista fyrirspurnina og opna aftur svargluggann **Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="8d111-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="8d111-358">Smelltu á **Í lagi** til að keyra áfyllingarsniðmátið.</span><span class="sxs-lookup"><span data-stu-id="8d111-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="8d111-359">Nú er áfyllingarvinna sköpuð til að taka til birgðir af svæðinu *MAGN* og fylla það á svæðið *GÓLF*.</span><span class="sxs-lookup"><span data-stu-id="8d111-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="8d111-360">Athugasemdir og ábendingar</span><span class="sxs-lookup"><span data-stu-id="8d111-360">Notes and tips</span></span>

<span data-ttu-id="8d111-361">Hér eru nokkrar athugasemdir og ábending til að vinna með eiginleikann:</span><span class="sxs-lookup"><span data-stu-id="8d111-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="8d111-362">Til að setja upp áfyllingarvinnu sem fer á viðeigandi svæði er hægt að tengja línur áfyllingarsniðmátsins og staðsetningarleiðbeiningar á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="8d111-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="8d111-363">Breyttu fyrirspurninni í haus staðsetningarleiðbeininganna og síaðu valda línur áfyllingarsniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="8d111-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="8d111-364">Notaðu leiðbeiningarkóða í línu áfyllingarsniðmátsins og láttu hann passa við staðsetningarleiðbeiningar frágangs.</span><span class="sxs-lookup"><span data-stu-id="8d111-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="8d111-365">Ef þú ert að nota kvikar staðsetningar verður áfyllingarvinnan búin annað hvort til fyrir fyrsta tiltæka staðsetningu eða fyrir staðsetningu sem er þegar með birgðum, ef aðgerð í staðsetningarleiðbeiningum er sett upp til að nota áætlun um **Sameiningu**.</span><span class="sxs-lookup"><span data-stu-id="8d111-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="8d111-366">Ef þú ert að nota fasta staðsetningar í stað svæða, ættir þú að nota [venjulega lágm./hám. áfyllingu](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="8d111-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
