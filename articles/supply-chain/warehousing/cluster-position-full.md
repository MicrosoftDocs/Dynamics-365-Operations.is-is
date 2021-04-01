---
title: Staðsetning klasa er full
description: Þetta efnisatriði veitir upplýsingar um eiginleikann fyrir fulla staðsetningu klasa. Þessi eiginleiki býður upp á aðra leið í stað ósveigjanlegar framkvæmdar á reglum um vinnuskiptingu þegar klasatiltekt er notuð, því að leyfð skekkjumörk rúmmálsins eru víðari fyrir gáma eða farm.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b6a7cad070377de58d21a8eb91ee3e1ffaf1c660
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233008"
---
# <a name="cluster-position-full"></a><span data-ttu-id="311ac-104">Staðsetning klasa er full</span><span class="sxs-lookup"><span data-stu-id="311ac-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="311ac-105">Eiginleikinn *Staðsetning klasa er full* býður upp á aðra leið í stað ósveigjanlegar framkvæmdar á reglum um vinnuskiptingu þegar klasatiltekt er notuð, því að leyfð skekkjumörk rúmmálsins eru víðari fyrir gáma eða farm.</span><span class="sxs-lookup"><span data-stu-id="311ac-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="311ac-106">Í algengum aðstæðum passa ekki öll atriði í verkbeiðni í valinn gám.</span><span class="sxs-lookup"><span data-stu-id="311ac-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="311ac-107">Starfsmenn vöruhúss sem sjá um klasatiltekt hafa nokkra valmöguleika í þessum aðstæðum: þeir verða annaðhvort að breyta yfir í stærri gám eða vinna með yfirmanninum sínum til að finna út betri lausn.</span><span class="sxs-lookup"><span data-stu-id="311ac-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="311ac-108">Þessi eiginleiki kynnir möguleikann á því að keyra hnappinn **Fullur** í einni vinnueiningunni í klasa.</span><span class="sxs-lookup"><span data-stu-id="311ac-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="311ac-109">Í eldri útgáfum var þessi valkostur aðeins tiltækur fyrir reglubundna tiltekt á pöntun, ekki fyrir klasatiltekt.</span><span class="sxs-lookup"><span data-stu-id="311ac-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="311ac-110">Þessi eiginleiki er hins vegar frábrugðinn hefðbundna hnappnum **Fullur** að því leyti að hann hættir við eftirstandandi vinnu.</span><span class="sxs-lookup"><span data-stu-id="311ac-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="311ac-111">Hann stingur ekki upp á að notandinn bæti öðru hólfi við sama klasann og hann stofnar ekki sjálfkrafa nýja vinnu.</span><span class="sxs-lookup"><span data-stu-id="311ac-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="311ac-112">Kveikja á eiginleika fyrir fulla staðsetningu klasa</span><span class="sxs-lookup"><span data-stu-id="311ac-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="311ac-113">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="311ac-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="311ac-114">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="311ac-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="311ac-115">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="311ac-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="311ac-116">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="311ac-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="311ac-117">**Heiti eiginleika:** *Staðsetning klasa er full*</span><span class="sxs-lookup"><span data-stu-id="311ac-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="311ac-118">Setja upp</span><span class="sxs-lookup"><span data-stu-id="311ac-118">Setup</span></span>

<span data-ttu-id="311ac-119">Þessi hluti býður upp á leiðarvísi og dæmi sem sýnir hvernig á að setja upp og nota eiginleikann *Staðsetning klasa er full*.</span><span class="sxs-lookup"><span data-stu-id="311ac-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="311ac-120">Gera sýnigögn tiltæk</span><span class="sxs-lookup"><span data-stu-id="311ac-120">Make sample data available</span></span>

<span data-ttu-id="311ac-121">Til að vinna í gegnum [sýniaðstæðurnar](#example-scenario) með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="311ac-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="311ac-122">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="311ac-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="311ac-123">Einnig er hægt að nota þetta sýnidæmi sem leiðsögn ef unnið er með þennan eiginleika í framleiðslukerfi.</span><span class="sxs-lookup"><span data-stu-id="311ac-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="311ac-124">Í því tilfelli verður hinsvegar að skipta út eigin gildum fyrir stillingarnar sem er lýst hér.</span><span class="sxs-lookup"><span data-stu-id="311ac-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="311ac-125">Klasanotandaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="311ac-125">Cluster profiles</span></span>

<span data-ttu-id="311ac-126">Tilgreina verður hvort klasaauðkenni eru sjálfkrafa mynduð, hversu margar stöður eru notaðar, hvenær klösum er skipt og hvernig tiltekt er raðað og staðfest.</span><span class="sxs-lookup"><span data-stu-id="311ac-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="311ac-127">Farðu á **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Klasaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="311ac-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="311ac-128">Í listasvæðinu skal velja færsluna **Stofna klasa**.</span><span class="sxs-lookup"><span data-stu-id="311ac-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="311ac-129">Í flýtiflipanum **Almennt** skal staðfesta eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="311ac-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="311ac-130">**Mynda klasaauðkenni:** *Já*</span><span class="sxs-lookup"><span data-stu-id="311ac-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="311ac-131">**Virkja stöður:** *Já*</span><span class="sxs-lookup"><span data-stu-id="311ac-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="311ac-132">**Fjöldi staða:** *2*</span><span class="sxs-lookup"><span data-stu-id="311ac-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="311ac-133">**Heiti stöðu:** *Tölustafur*</span><span class="sxs-lookup"><span data-stu-id="311ac-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="311ac-134">**Skipta klasaeiningu við:** *Frágang*</span><span class="sxs-lookup"><span data-stu-id="311ac-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="311ac-135">**Gerð röðunarstaðfestingar:** *Skönnun stöðu*</span><span class="sxs-lookup"><span data-stu-id="311ac-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="311ac-136">Í flýtiflipanum **Klasaröðun**.</span><span class="sxs-lookup"><span data-stu-id="311ac-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="311ac-137">Hnitanetið ætti að vera autt (það ætti ekki að innihalda neinar línur).</span><span class="sxs-lookup"><span data-stu-id="311ac-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="311ac-138">Vinnusniðmát</span><span class="sxs-lookup"><span data-stu-id="311ac-138">Work templates</span></span>

<span data-ttu-id="311ac-139">Tilgreina verður hvernig tiltekt fyrir klasatiltekt er búin til.</span><span class="sxs-lookup"><span data-stu-id="311ac-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="311ac-140">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="311ac-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="311ac-141">Efst á síðunni skal stilla reitinn **Gerð verkbeiðni** á *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="311ac-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="311ac-142">Gangið úr skugga um að eftirfarandi vinnusniðmát úr sýnigögnunum séu skráð.</span><span class="sxs-lookup"><span data-stu-id="311ac-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="311ac-143">Ef þau eru ekki tiltæk verður ekki hægt að ljúka atburðarásinni.</span><span class="sxs-lookup"><span data-stu-id="311ac-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="311ac-144">61 Stig sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="311ac-144">61 SO Stage</span></span>
    - <span data-ttu-id="311ac-145">61 Klasatiltekt sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="311ac-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="311ac-146">Staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="311ac-146">Location directives</span></span>

<span data-ttu-id="311ac-147">Tilgreina verður hvar vörur eru tíndar og hvar þær eru settar.</span><span class="sxs-lookup"><span data-stu-id="311ac-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="311ac-148">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="311ac-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="311ac-149">Efst í listanum skal stilla reitinn **Gerð verkbeiðni** á *Innkaupapantanir*.</span><span class="sxs-lookup"><span data-stu-id="311ac-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="311ac-150">Ganga skal úr skugga um að eftirfarandi leiðbeiningar sölupöntunar úr sýnigögnunum séu skráðar.</span><span class="sxs-lookup"><span data-stu-id="311ac-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="311ac-151">Ef þau eru ekki tiltæk verður ekki hægt að ljúka atburðarásinni.</span><span class="sxs-lookup"><span data-stu-id="311ac-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="311ac-152">61 Klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="311ac-152">61 Cluster pick</span></span>
    - <span data-ttu-id="311ac-153">61 Tiltektarröð sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="311ac-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="311ac-154">Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="311ac-154">Mobile device menu items</span></span>

<span data-ttu-id="311ac-155">Þú verður að stilla valmynd fartækis til að nota fyrirliggjandi vertk sem er stjórnað af klasatínslu.</span><span class="sxs-lookup"><span data-stu-id="311ac-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="311ac-156">Í valmyndaratriði fartækis fyrir klasatiltekt þarf að kveikja á færibreytunni **Leyfa skiptingu vinnu** og bæta verður við vinnuklasanum *Tiltekt sölupöntunar*.</span><span class="sxs-lookup"><span data-stu-id="311ac-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="311ac-157">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="311ac-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="311ac-158">Í listasvæðinu skal velja færsluna **Stofnun klasatiltektar**.</span><span class="sxs-lookup"><span data-stu-id="311ac-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="311ac-159">Veljið **Breyta** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="311ac-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="311ac-160">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="311ac-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="311ac-161">**Stjórnað af:** *Klasatiltekt*</span><span class="sxs-lookup"><span data-stu-id="311ac-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="311ac-162">**Mynda númeraplötu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="311ac-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="311ac-163">**Leyfa skiptingu vinnu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="311ac-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="311ac-164">**Prófílkenni klasa:** *Stofna klasa*</span><span class="sxs-lookup"><span data-stu-id="311ac-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="311ac-165">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="311ac-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="311ac-166">Í flýtiflipanum **Vinnuklasar** skal bæta við eftirfarandi tveimur línum eftir þörfum:</span><span class="sxs-lookup"><span data-stu-id="311ac-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="311ac-167">Lína 1 (oftast til staðar í sýnigögnum):</span><span class="sxs-lookup"><span data-stu-id="311ac-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="311ac-168">\**Auðkenni vinnuklasa:\*\*\*Sala*</span><span class="sxs-lookup"><span data-stu-id="311ac-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="311ac-169">**Gerð verkpöntunar:** *Sölupantanir*</span><span class="sxs-lookup"><span data-stu-id="311ac-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="311ac-170">Lína 2 (líklega ekki til staðar í sýnigögnum):</span><span class="sxs-lookup"><span data-stu-id="311ac-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="311ac-171">**Auðkenni vinnuklasa:** *Tiltekt sölupöntunar*</span><span class="sxs-lookup"><span data-stu-id="311ac-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="311ac-172">**Gerð verkpöntunar:** *Sölupantanir*</span><span class="sxs-lookup"><span data-stu-id="311ac-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="311ac-173">Farið í **Uppsetning verkstaðfestingar** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="311ac-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="311ac-174">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="311ac-174">Select **Edit**.</span></span>
1. <span data-ttu-id="311ac-175">Sláið inn eftirfarandi gildi í línunni í hnitaneti.</span><span class="sxs-lookup"><span data-stu-id="311ac-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="311ac-176">**Verkgerð** - *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="311ac-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="311ac-177">**Staðfesting afurðar** - *Velja gátreitinn*</span><span class="sxs-lookup"><span data-stu-id="311ac-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="311ac-178">Veljið **Vista** í aðgerðarúðunni og lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="311ac-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="311ac-179">Stofna tiltektarvinnu</span><span class="sxs-lookup"><span data-stu-id="311ac-179">Create picking work</span></span>

<span data-ttu-id="311ac-180">Áður en hægt er að ræsa klasatiltekt þarf að stofna einhverja vinnu á útleið.</span><span class="sxs-lookup"><span data-stu-id="311ac-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="311ac-181">Klasaforstillingin sem þú bjóst til áður tilgreinir tvær klasastöður.</span><span class="sxs-lookup"><span data-stu-id="311ac-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="311ac-182">Þess vegna þarf að stofna að minnsta kosti tvö vinnukenni fyrir tiltekt sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="311ac-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="311ac-183">Fyrir þessa atburðarás eiga færslur sér stað í vöruhúsi *61* og þær nota vörur *L0101* og *T0100*.</span><span class="sxs-lookup"><span data-stu-id="311ac-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="311ac-184">Sýnigögnin ættu að vera með nægar birgðir á lager af þessum vörum.</span><span class="sxs-lookup"><span data-stu-id="311ac-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="311ac-185">Gangið úr skugga um að nægilegar birgðir séu til staðar til að ljúka við færslurnar.</span><span class="sxs-lookup"><span data-stu-id="311ac-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="311ac-186">Stofna sölupöntun 1</span><span class="sxs-lookup"><span data-stu-id="311ac-186">Create sales order 1</span></span>

1. <span data-ttu-id="311ac-187">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="311ac-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="311ac-188">Veljið **Nýtt** til að búa til sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="311ac-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="311ac-189">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="311ac-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="311ac-190">**Viðskiptavinalykill:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="311ac-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="311ac-191">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="311ac-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="311ac-192">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="311ac-192">Select **OK**.</span></span>
1. <span data-ttu-id="311ac-193">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="311ac-193">The new sales order is opened.</span></span> <span data-ttu-id="311ac-194">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="311ac-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="311ac-195">**Vörunúmer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="311ac-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="311ac-196">**Magn:** *5*</span><span class="sxs-lookup"><span data-stu-id="311ac-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="311ac-197">Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Staðfest sendingardagsetning** á daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="311ac-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="311ac-198">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við annarri línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="311ac-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="311ac-199">**Vörunúmer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="311ac-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="311ac-200">**Magn:** *20*</span><span class="sxs-lookup"><span data-stu-id="311ac-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="311ac-201">Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Staðfest sendingardagsetning** á daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="311ac-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="311ac-202">Fyrir hverja línu sem bætt var við, skal fylgja þessum skrefum til að taka frá birgðir:</span><span class="sxs-lookup"><span data-stu-id="311ac-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="311ac-203">Velja skal línur sem á að taka frá.</span><span class="sxs-lookup"><span data-stu-id="311ac-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="311ac-204">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="311ac-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="311ac-205">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.</span><span class="sxs-lookup"><span data-stu-id="311ac-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="311ac-206">Lokaðu síðunni **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="311ac-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="311ac-207">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="311ac-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="311ac-208">Þegar losuninni er lokið birtast upplýsingaboð sem sýna auðkenni bylgju og sendingar sem voru búin til.</span><span class="sxs-lookup"><span data-stu-id="311ac-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="311ac-209">Stofna sölupöntun 2</span><span class="sxs-lookup"><span data-stu-id="311ac-209">Create sales order 2</span></span>

1. <span data-ttu-id="311ac-210">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="311ac-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="311ac-211">Veljið **Nýtt** til að búa til sölupöntun 2.</span><span class="sxs-lookup"><span data-stu-id="311ac-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="311ac-212">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="311ac-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="311ac-213">**Viðskiptavinalykill:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="311ac-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="311ac-214">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="311ac-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="311ac-215">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="311ac-215">Select **OK**.</span></span>
1. <span data-ttu-id="311ac-216">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="311ac-216">The new sales order is opened.</span></span> <span data-ttu-id="311ac-217">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="311ac-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="311ac-218">**Vörunúmer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="311ac-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="311ac-219">**Magn:** *20*</span><span class="sxs-lookup"><span data-stu-id="311ac-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="311ac-220">Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Staðfest sendingardagsetning** á daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="311ac-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="311ac-221">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við annarri línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="311ac-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="311ac-222">**Vörunúmer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="311ac-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="311ac-223">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="311ac-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="311ac-224">Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Staðfest sendingardagsetning** á daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="311ac-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="311ac-225">Fyrir hverja línu sem bætt var við, skal fylgja þessum skrefum til að taka frá birgðir:</span><span class="sxs-lookup"><span data-stu-id="311ac-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="311ac-226">Velja skal línur sem á að taka frá.</span><span class="sxs-lookup"><span data-stu-id="311ac-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="311ac-227">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="311ac-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="311ac-228">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.</span><span class="sxs-lookup"><span data-stu-id="311ac-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="311ac-229">Lokaðu síðunni **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="311ac-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="311ac-230">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="311ac-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="311ac-231">Þegar losuninni er lokið birtast upplýsingaboð sem sýna auðkenni bylgju og sendingar sem voru búin til.</span><span class="sxs-lookup"><span data-stu-id="311ac-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="311ac-232">Sækja vinnukenni og númer númeraplötu</span><span class="sxs-lookup"><span data-stu-id="311ac-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="311ac-233">Tvö vinnukenni ættu að hafa verið stofnuð, hvert þeirra með tveimur tiltektarlínum.</span><span class="sxs-lookup"><span data-stu-id="311ac-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="311ac-234">Fylgið eftirfarandi skrefum til að finna vinnukenni og úthlutanir númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="311ac-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="311ac-235">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="311ac-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="311ac-236">Í hnitanetinu **Yfirlit**, skal leita í dálknum **Pöntunarnúmer** að sölupöntununum tveimur sem voru stofnaðar rétt í þessu.</span><span class="sxs-lookup"><span data-stu-id="311ac-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="311ac-237">Skráið niður vinnuauðkenni hverrar sölupöntunar fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="311ac-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="311ac-238">Veljið línuna fyrir hvora sölupöntun fyrir sig til að sýna tengdar upplýsingar í hnitanetinu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="311ac-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="311ac-239">Skráið niður staðsetninguna þar sem hvor vara verður tínd úr.</span><span class="sxs-lookup"><span data-stu-id="311ac-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="311ac-240">Farið í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**.</span><span class="sxs-lookup"><span data-stu-id="311ac-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="311ac-241">Í aðgerðasvæðinu skal velja **Víddir** til að opna svargluggann **Birting víddar**.</span><span class="sxs-lookup"><span data-stu-id="311ac-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="311ac-242">Gangið úr skugga um að svargluggarnir **Númeraplata**, **Vöruhús** og **Vörunúmer** séu valdir og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="311ac-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="311ac-243">Í glugganum **Sía** skal stilla eftirfarandi síur:</span><span class="sxs-lookup"><span data-stu-id="311ac-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="311ac-244">**Vörunúmer** – **er eitt af** – *L0101* og *T100*</span><span class="sxs-lookup"><span data-stu-id="311ac-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="311ac-245">**Vöruhús** – **hefst á** – *61*</span><span class="sxs-lookup"><span data-stu-id="311ac-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="311ac-246">Skráið niður gildi **Númeraplötu** sem birtist.</span><span class="sxs-lookup"><span data-stu-id="311ac-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="311ac-247">Dæmi</span><span class="sxs-lookup"><span data-stu-id="311ac-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="311ac-248">Framkvæmd flæðis í fartæki - Uppsetning verkstaðfestingar fyrir afurðina</span><span class="sxs-lookup"><span data-stu-id="311ac-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="311ac-249">Skráðu þig inn í vöruhúsaforritið sem notandi í vöruhúsi *61*.</span><span class="sxs-lookup"><span data-stu-id="311ac-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="311ac-250">Farið í **Á útleið \> stofnun klasatiltektar**.</span><span class="sxs-lookup"><span data-stu-id="311ac-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="311ac-251">Síðan **VERK: Úthluta vinnu á klasa** birtist.</span><span class="sxs-lookup"><span data-stu-id="311ac-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="311ac-252">Færið inn vinnukennið fyrir sölupöntun 1 til að úthluta henni á klasastöðu 1.</span><span class="sxs-lookup"><span data-stu-id="311ac-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="311ac-253">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="311ac-254">Færið inn vinnukennið fyrir sölupöntun 2 til að úthluta henni á klasastöðu 2.</span><span class="sxs-lookup"><span data-stu-id="311ac-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="311ac-255">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="311ac-256">Síðan **VERK: Stofnun klasatiltektar: Tiltekt** birtist og sýnir *Vara L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="311ac-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="311ac-257">Vegna þess að klasaprófíllinn stillti fjölda staðsetninga á 2, beinir kerfið þér sjálfkrafa á fyrstu sameinuðu tiltektina: tvö bretti af vöru *L0101*.</span><span class="sxs-lookup"><span data-stu-id="311ac-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="311ac-258">Hvenær sem er í eftirfarandi skrefum er hægt að velja flipann **Upplýsingar** til að skoða viðbótarupplýsingar um verkið, t.d. tiltektarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="311ac-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="311ac-259">Stillið reitinn **VARA** á *L0101*.</span><span class="sxs-lookup"><span data-stu-id="311ac-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="311ac-260">Þetta staðfestir vörunúmerið, sem er krafist fyrir þetta valmyndaratriði (þetta var skilgreint áður með því að velja **Uppsetning verkstaðfestingar** á síðunni **Valmyndaratriði fartækis** þegar þetta valmyndaratriði var stofnað).</span><span class="sxs-lookup"><span data-stu-id="311ac-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="311ac-261">Sláið inn númeri númeraplötunnar sem tengist vörunni á staðsetningunni sem tínt er úr.</span><span class="sxs-lookup"><span data-stu-id="311ac-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="311ac-262">Þú munt velja tvö bretti.</span><span class="sxs-lookup"><span data-stu-id="311ac-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="311ac-263">Stillið reitinn **NP** á *NP\_TILTEKT\_01*.</span><span class="sxs-lookup"><span data-stu-id="311ac-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="311ac-264">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="311ac-265">Síðan **VERK: Raða: Stofnun klasatiltektar** birtist.</span><span class="sxs-lookup"><span data-stu-id="311ac-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="311ac-266">Hér raðar þú völdu brettunum tveimur á tiltektarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="311ac-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="311ac-267">Þessi staðsetning gæti verið tankur eða gámur sem er notaður til að aðskilja tíndar birgðar eftir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="311ac-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="311ac-268">Skoðið upplýsingarnar sem eru sýndar fyrir vöruna (*L0101*) og magn (*20* ea) sem verður raðað í stöðu 1 (fyrir sölupöntun 1).</span><span class="sxs-lookup"><span data-stu-id="311ac-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="311ac-269">Stillið reitinn **STAÐA NA** á *1*.</span><span class="sxs-lookup"><span data-stu-id="311ac-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="311ac-270">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="311ac-271">Skoðið upplýsingarnar sem eru sýndar fyrir vöruna (*L0101*) og magn (*20* ea) sem verður raðað í stöðu 2 (fyrir sölupöntun 2).</span><span class="sxs-lookup"><span data-stu-id="311ac-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="311ac-272">Stillið reitinn **STAÐA NA** á *2*.</span><span class="sxs-lookup"><span data-stu-id="311ac-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="311ac-273">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="311ac-274">Síðan **VERK: Stofnun klasatiltektar: Tiltekt** birtist og sýnir *Vara T0100 7 ea*.</span><span class="sxs-lookup"><span data-stu-id="311ac-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="311ac-275">Í þessari atburðarás getur staðsetning 1 ekki samþykkt fullt magn af vörum sem þarf að tína til að uppfylla sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="311ac-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="311ac-276">Staðan verður að vera merkt sem full.</span><span class="sxs-lookup"><span data-stu-id="311ac-276">A position must be marked as full.</span></span> <span data-ttu-id="311ac-277">Í þessu dæmi er hægt að gera hlutatínslu úr annarri vöru.</span><span class="sxs-lookup"><span data-stu-id="311ac-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="311ac-278">Önnur varan verður tínd að hluta til fyrir staðsetningu 1 og ný vinna verður stofnuð til að tína eftirstandandi magn til að uppfylla pöntunina.</span><span class="sxs-lookup"><span data-stu-id="311ac-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="311ac-279">Veljið valmyndarhnappinn (stundum kallaður hamborgari eða hamborgarahnappur) og veljið síðan **Staðsetningin er full**.</span><span class="sxs-lookup"><span data-stu-id="311ac-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="311ac-280">Auðkennið stöðuna sem er full og veljið *1*.</span><span class="sxs-lookup"><span data-stu-id="311ac-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="311ac-281">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="311ac-282">Færa skal inn magn tiltektar sem enn er hægt að tína í staðsetningu 1.</span><span class="sxs-lookup"><span data-stu-id="311ac-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="311ac-283">Kerfið getur ákveðið hvaða vörunúmer er verið að tína.</span><span class="sxs-lookup"><span data-stu-id="311ac-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="311ac-284">Færðu inn *2*.</span><span class="sxs-lookup"><span data-stu-id="311ac-284">Enter *2*.</span></span>
1. <span data-ttu-id="311ac-285">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="311ac-286">Staðfestið vörunúmerið til að ljúka við tínslu eftirstandandi vöru í stöðu 2.</span><span class="sxs-lookup"><span data-stu-id="311ac-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="311ac-287">Stillið reitinn **VARA** á *T0100*.</span><span class="sxs-lookup"><span data-stu-id="311ac-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="311ac-288">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="311ac-289">Færið inn númeraplötuna sem varan er tínd úr með því að stilla reitinn **NP** á *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="311ac-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="311ac-290">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="311ac-291">Skoðið upplýsingarnar sem eru sýndar fyrir vöruna (*T0100*) og magn (*2* ea) sem verður raðað í stöðu 2 (fyrir sölupöntun 2).</span><span class="sxs-lookup"><span data-stu-id="311ac-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="311ac-292">Stillið reitinn **STAÐA NA** á *2*.</span><span class="sxs-lookup"><span data-stu-id="311ac-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="311ac-293">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="311ac-294">Skoðið upplýsingarnar sem eru sýndar fyrir vöruna (*T0100*) og magn (*2* ea) sem verður raðað í stöðu 1 (fyrir sölupöntun 1).</span><span class="sxs-lookup"><span data-stu-id="311ac-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="311ac-295">Stillið reitinn **STAÐA NA** á *1*.</span><span class="sxs-lookup"><span data-stu-id="311ac-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="311ac-296">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="311ac-297">Síðan **VERK: Stofnun klasatiltektar: Frágangur** birtist.</span><span class="sxs-lookup"><span data-stu-id="311ac-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="311ac-298">Í þessari atburðarás hefur klasatiltekinni verið lokið og notandanum er sagt að ganga frá tíndum vörum úr staðsetningu 1 og staðsetningu 2 á geymslustaðsetningu *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="311ac-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="311ac-299">Fara skal yfir upplýsingarnar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="311ac-299">Review the information on the page.</span></span> <span data-ttu-id="311ac-300">Hún sýnir að heildarmagnið *44* verður sett á geymslustaðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="311ac-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="311ac-301">Veljið **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="311ac-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="311ac-302">Skilaboðin „Klasa er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="311ac-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="311ac-303">Nú er hægt að nota valmyndaratriðið **Tiltekt sölu** til að tína eftirstandandi magn.</span><span class="sxs-lookup"><span data-stu-id="311ac-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="311ac-304">Síðan er hægt að nota valmyndaratriðið **Hleðsla sölu** til að færa vörurnar úr geymslustaðsetningu yfir á dreifingarstað.</span><span class="sxs-lookup"><span data-stu-id="311ac-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]