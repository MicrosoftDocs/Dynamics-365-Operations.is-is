---
title: Flokkun bylgjusniðmáts
description: Flokkun bylgjusniðmáts gerir kerfinu kleift að nota uppsetningar bylgjusniðmáts til að ákvarða, byggt á skilyrðum sem skilgreind eru, hvernig skipta á losaðar línur og úthluta þeim á nýjar eða fyrirliggjandi bylgjur. Þessi eiginleiki getur verið gagnlegur í vöruhúsum þar sem bylgjur eru stofnaðar út frá tilteknum skilyrðum, en þar sem stjórnendur kjósa að stofna bylgjur sjálfkrafa í stað þess að gera það handvirkt.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a591624f6611148abe4888e67d8d3a9bbea9cd27
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838035"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="081aa-104">Flokkun bylgjusniðmáts</span><span class="sxs-lookup"><span data-stu-id="081aa-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="081aa-105">Flokkun bylgjusniðmáts gerir kerfinu kleift að nota uppsetningar [bylgjusniðmáts](tasks/configure-wave-processing.md) til að ákvarða, byggt á skilyrðum sem skilgreind eru, hvernig skipta á losaðar línur og úthluta þeim á nýjar eða fyrirliggjandi bylgjur.</span><span class="sxs-lookup"><span data-stu-id="081aa-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="081aa-106">Þessi eiginleiki getur verið gagnlegur í vöruhúsum þar sem bylgjur eru stofnaðar út frá tilteknum skilyrðum, en þar sem stjórnendur kjósa að stofna bylgjur sjálfkrafa í stað þess að gera það handvirkt.</span><span class="sxs-lookup"><span data-stu-id="081aa-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="081aa-107">Hann gerir kerfunum kleift að bæta sérhverri nýlega losaðri sendingu við fyrstu bylgjuna sem það finnur sem er með samsvarandi reitargildi flokkunar.</span><span class="sxs-lookup"><span data-stu-id="081aa-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="081aa-108">Ef engin samsvörun finnst stofnar kerfið nýja bylgju fyrir nýju sendinguna.</span><span class="sxs-lookup"><span data-stu-id="081aa-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="081aa-109">Flokkun bylgjusniðmáts er ekki studd fyrir vinnugerðirnar *hráefnistiltekt framleiðslu* eða *Kanban-tiltekt*.</span><span class="sxs-lookup"><span data-stu-id="081aa-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="081aa-110">Þetta er vegna þess að bylgjuflokkun er byggð á sendingum og þessar vinnugerðir nota ekki sendingar.</span><span class="sxs-lookup"><span data-stu-id="081aa-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="081aa-111">Kveikja á eiginleika bylgjusniðmátsflokkunar</span><span class="sxs-lookup"><span data-stu-id="081aa-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="081aa-112">Áður en hægt er að nota eiginleikann *Flokkun bylgjusniðmáts* verður að vera kveikt á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="081aa-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="081aa-113">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="081aa-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="081aa-114">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="081aa-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="081aa-115">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="081aa-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="081aa-116">**Heiti eiginleika:** *Flokkun bylgjusniðmáts*</span><span class="sxs-lookup"><span data-stu-id="081aa-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="081aa-117">Stilla bylgjusniðmát til að nota flokkun bylgjusniðmáts</span><span class="sxs-lookup"><span data-stu-id="081aa-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="081aa-118">Til að gera bylgjusniðmátsflokkun tiltæka skal fylgja þessum skrefum til að setja upp [bylgjusniðmát](tasks/configure-wave-processing.md).</span><span class="sxs-lookup"><span data-stu-id="081aa-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="081aa-119">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="081aa-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="081aa-120">Vinstra megin á svæðinu skal velja bylgjusniðmátið sem á að setja upp.</span><span class="sxs-lookup"><span data-stu-id="081aa-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="081aa-121">Ef verið er að undirbúa vinnu í gegnum atburðarásina síðar í þessu efnisatriði með því að nota sýnigögn skal velja sniðmátið **62 Sjálfgefin sending**.</span><span class="sxs-lookup"><span data-stu-id="081aa-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="081aa-122">Veldu **Breyta** til að setja síðuna í breytingastillingu.</span><span class="sxs-lookup"><span data-stu-id="081aa-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="081aa-123">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="081aa-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="081aa-124">**Gera stofnun bylgju sjálfvirka:** *Já*</span><span class="sxs-lookup"><span data-stu-id="081aa-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="081aa-125">**Úthluta á opnar bylgjur:** *Já*</span><span class="sxs-lookup"><span data-stu-id="081aa-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="081aa-126">**Vinna úr bylgju við losun í vörugeymslu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="081aa-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="081aa-127">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna fyrirspurnargluggann.</span><span class="sxs-lookup"><span data-stu-id="081aa-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="081aa-128">Í fyrirspurnarglugganum, í flipanum **Röðun**, skal fara yfir skilyrði röðunar og ganga úr skugga um að til sé regla sem tekur með reitinn sem ætlunin er að nota til að flokka bylgjurnar.</span><span class="sxs-lookup"><span data-stu-id="081aa-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="081aa-129">Ef verið er að undirbúa vinnu í gegnum atburðarásina með því að nota sýnigögn, skal bæta við línu sem er með eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="081aa-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="081aa-130">**Tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="081aa-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="081aa-131">**Afleidd tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="081aa-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="081aa-132">**Reitur:** *Flutningsþjónusta*</span><span class="sxs-lookup"><span data-stu-id="081aa-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="081aa-133">Þegar þetta gildi er valið gætu komið upp eftirfarandi skilaboð: „Reiturinn Flutningsþjónusta er ekki vísisreitur.</span><span class="sxs-lookup"><span data-stu-id="081aa-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="081aa-134">Á að bæta við röðun á þetta?“</span><span class="sxs-lookup"><span data-stu-id="081aa-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="081aa-135">Veljið **Já** til að bæta við röðun.</span><span class="sxs-lookup"><span data-stu-id="081aa-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="081aa-136">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="081aa-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="081aa-137">Veljið **Í lagi** til að vista breytingarnar og loka fyrirspurnarglugganum.</span><span class="sxs-lookup"><span data-stu-id="081aa-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="081aa-138">Á aðgerðasvæðinu skal velja **Flokkun bylgjusniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="081aa-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="081aa-139">Á síðunni **Flokkun bylgjusniðmáts** skal velja gátreitinn **Flokka eftir** fyrir hverja línu sem nota á til að flokka pöntunarlínurnar í bylgjur, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="081aa-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="081aa-140">Ef verið er að undirbúa vinnu í gegnum aðstæðurnar með því að nota sýnigögn skal velja gátreitinn **Flokka eftir** fyrir línuna *Flutningsþjónusta*.</span><span class="sxs-lookup"><span data-stu-id="081aa-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="081aa-141">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="081aa-141">Select **Save**.</span></span>
1. <span data-ttu-id="081aa-142">Lokið síðunni **Flokkun bylgjusniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="081aa-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="081aa-143">Veljið **Vista** til að vista sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="081aa-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="081aa-144">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="081aa-144">Scenario</span></span>

<span data-ttu-id="081aa-145">Þessi hluti býður upp á forskrift sem hægt er að vinna með til að fá upplýsingar um hvað þessi eiginleiki gerir og hvernig á að vinna með hann.</span><span class="sxs-lookup"><span data-stu-id="081aa-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="081aa-146">Gera sýnigögn tiltæk</span><span class="sxs-lookup"><span data-stu-id="081aa-146">Make sample data available</span></span>

<span data-ttu-id="081aa-147">Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp.</span><span class="sxs-lookup"><span data-stu-id="081aa-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="081aa-148">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="081aa-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="081aa-149">Einnig er hægt að nota þessar aðstæður sem leiðsögn um notkun á eiginleikanum þegar unnið er í framleiðslukerfi.</span><span class="sxs-lookup"><span data-stu-id="081aa-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="081aa-150">Í slíku tilfelli þarf hinsvegar að skipta út eigin gildum og einhverjar nauðsynlegar færslugerðir gæti vantað sem stöðluðu sýnigögnin bjóða upp á.</span><span class="sxs-lookup"><span data-stu-id="081aa-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="081aa-151">Aðstæður: Flokkun bylgjusniðmáts</span><span class="sxs-lookup"><span data-stu-id="081aa-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="081aa-152">Þessar aðstæður sýna hvernig nota má flokkun bylgjusniðmáts til að stofna sjálfkrafa margar bylgjur, byggðar á flokkunarskilyrðum sem eru skilgreind í bylgjusniðmáti.</span><span class="sxs-lookup"><span data-stu-id="081aa-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="081aa-153">Í þessum aðstæðum er bylgjusniðmátið sett upp í kerfinu til að búa til eina bylgju á flutningsþjónustu.</span><span class="sxs-lookup"><span data-stu-id="081aa-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="081aa-154">Áður en hafist er handa þarf að undirbúa bylgjusniðmátið eins og lýst er í hlutanum [Stilla bylgjusniðmát til að nota flokkun bylgjusniðmáts](#set-up-template) fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="081aa-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="081aa-155">Ef unnið verður með sýnigögn fyrir þetta dæmi skal gæta þess að nota gildi sýnigagnanna sem stungið er upp á í því ferli.</span><span class="sxs-lookup"><span data-stu-id="081aa-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="081aa-156">Þessi uppsetning mun flokka bylgjurnar samkvæmt flutningsþjónustunni sem er stillt fyrir hverja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="081aa-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="081aa-157">Stofna sölupöntun 1</span><span class="sxs-lookup"><span data-stu-id="081aa-157">Create sales order 1</span></span>

1. <span data-ttu-id="081aa-158">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="081aa-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="081aa-159">Smellið á **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="081aa-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="081aa-160">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="081aa-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="081aa-161">Í flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á *US-004*.</span><span class="sxs-lookup"><span data-stu-id="081aa-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="081aa-162">Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *62*.</span><span class="sxs-lookup"><span data-stu-id="081aa-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="081aa-163">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum **Stofna sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="081aa-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="081aa-164">Nýja sölupöntunin er opnuð í **Línur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="081aa-165">Skráið hjá ykkur sölupöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="081aa-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="081aa-166">Skiptið yfir í **Hausa** yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="081aa-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="081aa-167">Í flýtiflipanum **Afhending**, í hlutanum **Flutningur**, skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="081aa-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="081aa-168">**Farmflytjandi:** *Flugfarmur*</span><span class="sxs-lookup"><span data-stu-id="081aa-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="081aa-169">**Flutningsþjónusta:** *flug*</span><span class="sxs-lookup"><span data-stu-id="081aa-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="081aa-170">Skiptið aftur yfir í yfirlitið **Línur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="081aa-171">Í hlutanum **Sölupöntunarlínur** skal velja **Bæta við línu** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="081aa-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="081aa-172">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="081aa-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="081aa-173">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="081aa-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="081aa-174">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="081aa-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="081aa-175">Veljið nýju pöntunarlínuna og síðan í valmyndinni **Birgðir** fyrir ofan hnitanetið skal smella á **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="081aa-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="081aa-176">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="081aa-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="081aa-177">Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="081aa-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="081aa-178">Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="081aa-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="081aa-179">Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun.</span><span class="sxs-lookup"><span data-stu-id="081aa-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="081aa-180">Skráið hjá ykkur bylgjukennið og sendingarkenni.</span><span class="sxs-lookup"><span data-stu-id="081aa-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="081aa-181">Skoða bylgjuna sem var búin til úr sölupöntun 1</span><span class="sxs-lookup"><span data-stu-id="081aa-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="081aa-182">Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="081aa-183">Veljið bylgjukennið sem stofnað var í sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="081aa-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="081aa-184">Veljið tengil bylgjukennis til að opna upplýsingasíðu bylgjunnar.</span><span class="sxs-lookup"><span data-stu-id="081aa-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="081aa-185">Takið eftir að sendingunni hefur verið bætt við flýtiflipann **Bylgjulínur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="081aa-186">Stofna sölupöntun 2</span><span class="sxs-lookup"><span data-stu-id="081aa-186">Create sales order 2</span></span>

1. <span data-ttu-id="081aa-187">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="081aa-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="081aa-188">Smellið á **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="081aa-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="081aa-189">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="081aa-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="081aa-190">Í flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á *US-005*.</span><span class="sxs-lookup"><span data-stu-id="081aa-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="081aa-191">Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *62*.</span><span class="sxs-lookup"><span data-stu-id="081aa-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="081aa-192">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum **Stofna sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="081aa-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="081aa-193">Nýja sölupöntunin er opnuð í **Línur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="081aa-194">Skráið hjá ykkur sölupöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="081aa-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="081aa-195">Skiptið yfir í **Hausa** yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="081aa-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="081aa-196">Í flýtiflipanum **Afhending**, í hlutanum **Flutningur**, skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="081aa-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="081aa-197">**Farmflytjandi:** *Blómaflytjandi*</span><span class="sxs-lookup"><span data-stu-id="081aa-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="081aa-198">**Flutningsþjónusta:** *Std*</span><span class="sxs-lookup"><span data-stu-id="081aa-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="081aa-199">Skiptið aftur yfir í yfirlitið **Línur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="081aa-200">Í hlutanum **Sölupöntunarlínur** skal velja **Bæta við línu** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="081aa-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="081aa-201">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="081aa-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="081aa-202">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="081aa-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="081aa-203">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="081aa-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="081aa-204">Veljið nýju pöntunarlínuna og síðan í valmyndinni **Birgðir** fyrir ofan hnitanetið skal smella á **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="081aa-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="081aa-205">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="081aa-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="081aa-206">Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="081aa-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="081aa-207">Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="081aa-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="081aa-208">Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun.</span><span class="sxs-lookup"><span data-stu-id="081aa-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="081aa-209">Skráið hjá ykkur bylgjukennið og sendingarkenni.</span><span class="sxs-lookup"><span data-stu-id="081aa-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="081aa-210">Takið eftir því að bylgjukennið er ólíkt bylgjukenni fyrstu sölupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="081aa-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="081aa-211">Skoða bylgjuna sem var búin til úr sölupöntun 2</span><span class="sxs-lookup"><span data-stu-id="081aa-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="081aa-212">Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="081aa-213">Veljið bylgjukennið sem stofnað var í sölupöntun tvö.</span><span class="sxs-lookup"><span data-stu-id="081aa-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="081aa-214">Veljið tengil bylgjukennis til að opna upplýsingasíðu bylgjunnar.</span><span class="sxs-lookup"><span data-stu-id="081aa-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="081aa-215">Takið eftir að sendingunni hefur verið bætt við flýtiflipann **Bylgjulínur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="081aa-216">Ný bylgja var stofnuð fyrir þessa sendingu vegna þess að hún notar aðra flutningsþjónustu en fyrsta sölupöntunin.</span><span class="sxs-lookup"><span data-stu-id="081aa-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="081aa-217">Stofna sölupöntun 3</span><span class="sxs-lookup"><span data-stu-id="081aa-217">Create sales order 3</span></span>

1. <span data-ttu-id="081aa-218">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="081aa-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="081aa-219">Smellið á **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="081aa-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="081aa-220">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="081aa-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="081aa-221">Í flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á *US-006*.</span><span class="sxs-lookup"><span data-stu-id="081aa-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="081aa-222">Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *62*.</span><span class="sxs-lookup"><span data-stu-id="081aa-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="081aa-223">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum **Stofna sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="081aa-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="081aa-224">Nýja sölupöntunin er opnuð í **Línur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="081aa-225">Skráið hjá ykkur sölupöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="081aa-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="081aa-226">Skiptið yfir í **Hausa** yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="081aa-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="081aa-227">Í flýtiflipanum **Afhending**, í hlutanum **Flutningur**, skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="081aa-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="081aa-228">**Farmflytjandi:** *Flugfarmur*</span><span class="sxs-lookup"><span data-stu-id="081aa-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="081aa-229">**Flutningsþjónusta:** *flug*</span><span class="sxs-lookup"><span data-stu-id="081aa-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="081aa-230">Skiptið aftur yfir í yfirlitið **Línur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="081aa-231">Í hlutanum **Sölupöntunarlínur** skal velja **Bæta við línu** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="081aa-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="081aa-232">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="081aa-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="081aa-233">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="081aa-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="081aa-234">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="081aa-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="081aa-235">Veljið nýju pöntunarlínuna og síðan í valmyndinni **Birgðir** fyrir ofan hnitanetið skal smella á **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="081aa-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="081aa-236">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="081aa-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="081aa-237">Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="081aa-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="081aa-238">Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="081aa-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="081aa-239">Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun.</span><span class="sxs-lookup"><span data-stu-id="081aa-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="081aa-240">Skráið hjá ykkur bylgjukennið og sendingarkenni.</span><span class="sxs-lookup"><span data-stu-id="081aa-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="081aa-241">Sendingunni hefur verið úthlutað á fyrirliggjandi bylgju úr fyrstu sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="081aa-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="081aa-242">Skoða bylgjuna fyrir sölupantanir 1 og 3</span><span class="sxs-lookup"><span data-stu-id="081aa-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="081aa-243">Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="081aa-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="081aa-244">Veljið bylgjukennið sem stofnað var í þriðju sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="081aa-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="081aa-245">Veljið tengil bylgjukennis til að opna upplýsingasíðu bylgjunnar.</span><span class="sxs-lookup"><span data-stu-id="081aa-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="081aa-246">Takið eftir að sendingunni hefur verið bætt við flýtiflipann **Bylgjulínur**, ásamt sendingunni fyrir fyrstu sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="081aa-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]