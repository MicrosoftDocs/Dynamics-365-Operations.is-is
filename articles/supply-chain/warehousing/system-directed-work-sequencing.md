---
title: Kerfisstýrð vinnuröðun
description: Þetta efnisatriði veitir upplýsingar um kerfisstýrða vinnuröðun. Þessi aðgerð gerir þér kleift að flokka og sía verkbeiðnir sem kerfið býður notendum til framkvæmdar. Það er gagnlegt við aðstæður þar sem þörf er á viðbótarskilyrðum til að keyra tiltektarferli vöruhússins.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7db884a5cd62e1f44a2a86316fde6bf2d11a3376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239135"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="174bf-105">Kerfisstýrð vinnuröðun</span><span class="sxs-lookup"><span data-stu-id="174bf-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="174bf-106">Kerfisstýrð vinnuröðun gerir þér kleift að flokka og sía verkbeiðnir sem kerfið býður notendum til framkvæmdar.</span><span class="sxs-lookup"><span data-stu-id="174bf-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="174bf-107">Það er gagnlegt við aðstæður þar sem þörf er á viðbótarskilyrðum (t.d. tímasetningu sendingar, tiltektarsvæði, staðsetningarforstillingu eða sambland ólíkra skilyrða) til að keyra tiltektarferli vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="174bf-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="174bf-108">Þessi virkni víkkar út núverandi kerfisstýrða tiltektaraðgerð með því að bæta við kerfisstýrðri fyrirspurnapöntun þar sem notendur geta sett upp röð og eina eða fleiri fyrirspurnir sem munu meta allar verkbeiðnir sem eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="174bf-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="174bf-109">Aðeins verkbeiðnir sem uppfylla skilyrðin sem eru tilgreind í uppsetningu valmyndaratriðis í fartækinu verða fangaðar og kynntar.</span><span class="sxs-lookup"><span data-stu-id="174bf-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="174bf-110">Þess vegna gerir þessi virkni kleift frekari fínstillingu á tiltektarferlum vöruhússins þar sem hún greinir verkbeiðnir sem samsvara tilgreindum skilyrðum, úthlutar þeim á rétt valmyndaratriði fartækisins og birtir síðan starfsmanni, miðað við tiltekinn hæfnigrunn, búnað við tiltekt eða önnur skilyrði.</span><span class="sxs-lookup"><span data-stu-id="174bf-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="174bf-111">Nota verður mörg valmyndaratriði fartækisins ef þörf er á öðrum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="174bf-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="174bf-112">Kveikja á eiginleikanum kerfisstýrð vinnuröðun fyrir alla stofnunina/fyrirtækið</span><span class="sxs-lookup"><span data-stu-id="174bf-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="174bf-113">Áður en þú getur notað kerfisstýrða vinnuröðun verður að vera kveikt á eiginleikanum í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="174bf-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="174bf-114">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="174bf-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="174bf-115">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="174bf-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="174bf-116">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="174bf-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="174bf-117">**Heiti eiginleika:** *Kerfisstýrð vinnuröðun fyrir alla stofnunina/fyrirtækið*</span><span class="sxs-lookup"><span data-stu-id="174bf-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="174bf-118">Setja upp</span><span class="sxs-lookup"><span data-stu-id="174bf-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="174bf-119">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="174bf-119">Make demo data available</span></span>

<span data-ttu-id="174bf-120">Til að vinna í gegnum aðstæðurnar með því að nota gildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu sýnigögnin eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="174bf-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="174bf-121">Þar að auki verður þú að velja **USMF**-lögaðila.</span><span class="sxs-lookup"><span data-stu-id="174bf-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="174bf-122">Aðstæðurnar nota vöruhús *51* úr sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="174bf-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="174bf-123">Áður en þú losar pantanir til vöruhússins skaltu ganga úr skugga um að tiltektarstaðsetningar hafi nægar birgðir fyrir öll atriðin á pöntunum.</span><span class="sxs-lookup"><span data-stu-id="174bf-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="174bf-124">Sjálfgefin USMF-gögn ættu að styðja þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="174bf-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="174bf-125">Ef þú notar ekki sýnigögn skaltu skoða stillingu **Staðsetningarleiðbeininga** til að komast að því hvaða tiltektarstaðsetningar eru notaðar við tiltekt sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="174bf-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="174bf-126">Ef þú verður að breyta birgðum geturðu búið til handvirkar birgðahreyfingar, notað áfyllingu eða notað hvaða annað flæði sem er.</span><span class="sxs-lookup"><span data-stu-id="174bf-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="174bf-127">Setja upp valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="174bf-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="174bf-128">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="174bf-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="174bf-129">Veldu **Tiltekt sölu – Kerfi** á listanum yfir valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="174bf-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="174bf-130">Áskilið valmyndaratriði ætti þegar að vera til.</span><span class="sxs-lookup"><span data-stu-id="174bf-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="174bf-131">Staðfestið eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="174bf-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="174bf-132">Á flýtiflipanum **Almennt** ætti svæðið **Stjórnað af** að vera stillt á *Kerfisstýrt*.</span><span class="sxs-lookup"><span data-stu-id="174bf-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="174bf-133">Flýtiflipinn **Vinnuklasar** ætti að sýna eftirfarandi stillingar.</span><span class="sxs-lookup"><span data-stu-id="174bf-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="174bf-134">Auðkenni vinnuklasa</span><span class="sxs-lookup"><span data-stu-id="174bf-134">Work class ID</span></span> | <span data-ttu-id="174bf-135">Gerð verkpöntunar</span><span class="sxs-lookup"><span data-stu-id="174bf-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="174bf-136">Sala</span><span class="sxs-lookup"><span data-stu-id="174bf-136">Sales</span></span> | <span data-ttu-id="174bf-137">Sölupantanir</span><span class="sxs-lookup"><span data-stu-id="174bf-137">Sales orders</span></span> |
        | <span data-ttu-id="174bf-138">Tiltekt sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="174bf-138">SO Pick</span></span> | <span data-ttu-id="174bf-139">Sölupantanir</span><span class="sxs-lookup"><span data-stu-id="174bf-139">Sales orders</span></span> |

1. <span data-ttu-id="174bf-140">Á aðgerðarsvæðinu velur þú **Kerfisstýrðar fyrirspurnir vinnuröðunar**.</span><span class="sxs-lookup"><span data-stu-id="174bf-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="174bf-141">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="174bf-141">Select **Edit**.</span></span>
1. <span data-ttu-id="174bf-142">Eyða núverandi línu og staðfestu síðan aðgerðina með því að velja **Já**.</span><span class="sxs-lookup"><span data-stu-id="174bf-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="174bf-143">Veldu **Nýtt** á aðgerðasvæðinu til að búa til línu.</span><span class="sxs-lookup"><span data-stu-id="174bf-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="174bf-144">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="174bf-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="174bf-145">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="174bf-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="174bf-146">**Lýsingarsvæði:** *Vinnumagn minna en 20 og fer minnkandi*</span><span class="sxs-lookup"><span data-stu-id="174bf-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="174bf-147">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="174bf-147">Select **Save**.</span></span>
1. <span data-ttu-id="174bf-148">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="174bf-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="174bf-149">Á flipanum **Samtengingar** skaltu stækka stigveldi samtengingar til að sýna töfluna **Vinnulínur**.</span><span class="sxs-lookup"><span data-stu-id="174bf-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="174bf-150">Veldu töflutenginguna **Vinnulínur**.</span><span class="sxs-lookup"><span data-stu-id="174bf-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="174bf-151">Velja **Bæta við töflusamtengingu**.</span><span class="sxs-lookup"><span data-stu-id="174bf-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="174bf-152">Finndu og veldu línuna á listanum sem birtist sem hefur eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="174bf-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="174bf-153">**Samtengingarstilling:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="174bf-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="174bf-154">**Tengsl:** *Staðsetningar (Staðsetning)*</span><span class="sxs-lookup"><span data-stu-id="174bf-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="174bf-155">Veljið **Velja**.</span><span class="sxs-lookup"><span data-stu-id="174bf-155">Select **Select**.</span></span>

    <span data-ttu-id="174bf-156">Staðsetningum er bætt við töflutenginguna.</span><span class="sxs-lookup"><span data-stu-id="174bf-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="174bf-157">Veldu **Bæta við** til að bæta við röð á flipanum **Röðun**.</span><span class="sxs-lookup"><span data-stu-id="174bf-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="174bf-158">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="174bf-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="174bf-159">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="174bf-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="174bf-160">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="174bf-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="174bf-161">**Svæði:** *Vinnumagn* (Í skilaboðaglugganum sem birtist skaltu velja **Já** til að bæta flokkun við þetta svæði).</span><span class="sxs-lookup"><span data-stu-id="174bf-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="174bf-162">**Leitarstefna:** *Lækkandi*</span><span class="sxs-lookup"><span data-stu-id="174bf-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="174bf-163">Smellt er á flipann **Svið**.</span><span class="sxs-lookup"><span data-stu-id="174bf-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="174bf-164">Ef aðeins skal hafa sérstök vinnuskilyrði í röðinni, geturðu tilgreint þau á flipanum **Svið**. Í þessu dæmi viltu aðeins taka með vinnu þar sem magnið er minna en 20 ea (lægsta mælieiningin).</span><span class="sxs-lookup"><span data-stu-id="174bf-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="174bf-165">Athugaðu að tilteknar línur eru þegar innifaldar.</span><span class="sxs-lookup"><span data-stu-id="174bf-165">Notice that some lines are already included.</span></span> <span data-ttu-id="174bf-166">Ekki ætti að fjarlægja þessar línur.</span><span class="sxs-lookup"><span data-stu-id="174bf-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="174bf-167">Smellið á **Bæta við** til að bæta við nýrri línu.</span><span class="sxs-lookup"><span data-stu-id="174bf-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="174bf-168">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="174bf-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="174bf-169">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="174bf-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="174bf-170">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="174bf-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="174bf-171">**Svæði:** *Vinnumagn birgða*</span><span class="sxs-lookup"><span data-stu-id="174bf-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="174bf-172">**Skilyrði:** *\<20* (minna en 20)</span><span class="sxs-lookup"><span data-stu-id="174bf-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="174bf-173">Smellið á **Bæta við** til að bæta við annarri línu.</span><span class="sxs-lookup"><span data-stu-id="174bf-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="174bf-174">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="174bf-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="174bf-175">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="174bf-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="174bf-176">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="174bf-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="174bf-177">**Svæði:** *Gerð vinnu*</span><span class="sxs-lookup"><span data-stu-id="174bf-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="174bf-178">**Skilyrði:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="174bf-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="174bf-179">Smellið á **Bæta við** til að bæta við annarri línu.</span><span class="sxs-lookup"><span data-stu-id="174bf-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="174bf-180">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="174bf-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="174bf-181">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="174bf-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="174bf-182">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="174bf-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="174bf-183">**Reitur:** *Auðkenni forstillingar staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="174bf-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="174bf-184">**Skilyrði:** *!STIG*</span><span class="sxs-lookup"><span data-stu-id="174bf-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="174bf-185">Gættu þess að setja upphrópunarmerki (*!*) fyrir framan *STIG*..</span><span class="sxs-lookup"><span data-stu-id="174bf-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="174bf-186">Veldu **Í lagi** til að vista og loka fyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="174bf-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="174bf-187">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="174bf-187">Select **Save**.</span></span>
1. <span data-ttu-id="174bf-188">Lokið síðunni til að fara aftur á síðuna **Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="174bf-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="174bf-189">Þessi uppsetning skilgreinir skilyrðin sem verða notuð til að mata valmyndaratriði fartækis með tækri vinnu.</span><span class="sxs-lookup"><span data-stu-id="174bf-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="174bf-190">Ef þú bætir fleiri skilyrðalínum við fyrirspurnina mun kerfið nota fyrirspurnalínuna sem hefur lægsta raðnúmer fyrst.</span><span class="sxs-lookup"><span data-stu-id="174bf-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="174bf-191">Með öðrum orðum, öll tæk vinna fyrir raðnúmer 1 verða kynnt notandanum fyrst og síðan öll vinna fyrir raðnúmer 2.</span><span class="sxs-lookup"><span data-stu-id="174bf-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="174bf-192">Þess vegna, ef nota þarf tiltekið svið og flokkun saman, ætti að tilgreina þau í sömu fyrirspurninni fyrir kerfisstýrðu vinnuröðina.</span><span class="sxs-lookup"><span data-stu-id="174bf-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="174bf-193">Þessi uppsetning fangar alla vinnu sem hafa að minnsta kosti eina línu þar sem magnið er minna en 20 ea.</span><span class="sxs-lookup"><span data-stu-id="174bf-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="174bf-194">Þess vegna, ef vinnan hefur línu þar sem magnið er nákvæmlega 20 ea eða meira en 20 ea, mun það vera gilt, að því tilskildu að það hafi einnig að minnsta kosti eina línu þar sem magnið er minna en 20 ea.</span><span class="sxs-lookup"><span data-stu-id="174bf-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="174bf-195">Staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="174bf-195">Location directives</span></span>

<span data-ttu-id="174bf-196">Ef þú ert að nota sjálfgefin Contoso gögn þarf ekki að breyta fyrirspurninni um aðgerðir í staðsetningarleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="174bf-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="174bf-197">Hins vegar, til að ganga úr skugga um að staðsetningarleiðbeiningarnar fangi atriðin í sölupöntunum þegar þú notar aðgerðina í umhverfi sem ekki er frá Contoso skaltu búa til nýjar staðsetningarleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="174bf-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="174bf-198">Fylgdu þessum skrefum til að staðfesta stillingarnar í sýniútgáfuumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="174bf-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="174bf-199">Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="174bf-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="174bf-200">Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="174bf-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="174bf-201">Veldu staðsetningarleiðbeiningarnar sem heita *51 Tiltekt*.</span><span class="sxs-lookup"><span data-stu-id="174bf-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="174bf-202">Á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** velur þú línuna fyrir aðgerðina **Tiltekt**.</span><span class="sxs-lookup"><span data-stu-id="174bf-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="174bf-203">Veldu **Breyta fyrirspurn** fyrir ofan hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="174bf-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="174bf-204">Farðu aftur yfir fyrirspurnina **Svið**.</span><span class="sxs-lookup"><span data-stu-id="174bf-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="174bf-205">Leitaðu að línunni þar sem svæðið **Svæði** er stillt á *Staðsetning*.</span><span class="sxs-lookup"><span data-stu-id="174bf-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="174bf-206">Gakktu úr skugga um að svæðið **Skilyrði** sé autt (þ.e. að engar takmarkanir séu til staðar).</span><span class="sxs-lookup"><span data-stu-id="174bf-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="174bf-207">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="174bf-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="174bf-208">Búa til tiltektarvinnu sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="174bf-208">Create sales order picking work</span></span>

<span data-ttu-id="174bf-209">Áður en kerfisstýrð tiltekt er keyrð ætti að búa til einhverja vinnu á útleið.</span><span class="sxs-lookup"><span data-stu-id="174bf-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="174bf-210">Fyrir þessar aðstæður muntu búa til fjórar sölupantanir sem eru byggðar á tilgreindum fyrirspurnum um kerfisstýrða vinnuröð.</span><span class="sxs-lookup"><span data-stu-id="174bf-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="174bf-211">Hægt er að taka frá birgðir sjálfkrafa fyrir hverja sölupöntun fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="174bf-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="174bf-212">Þar af leiðand er ekki hægt að taka fráteknar birgðir út úr vöruhúsi fyrir aðra pöntun nema birgðafrátektin eða hluti birgðafrátekningar sé afturkölluð.</span><span class="sxs-lookup"><span data-stu-id="174bf-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="174bf-213">Þú losar síðan hverja sölupöntun til vöruhússins til að búa til vinnu á útleið.</span><span class="sxs-lookup"><span data-stu-id="174bf-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="174bf-214">Sölupöntun 1</span><span class="sxs-lookup"><span data-stu-id="174bf-214">Sales order 1</span></span>

1. <span data-ttu-id="174bf-215">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="174bf-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="174bf-216">Í aðgerðarúðunni velurðu **Nýtt** til að búa til sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="174bf-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="174bf-217">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="174bf-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="174bf-218">Í hlutanum **Viðskiptavinur** skaltu stilla svæðið **Viðskiptavinalykill** á *US-004*.</span><span class="sxs-lookup"><span data-stu-id="174bf-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="174bf-219">Í hlutanum **Almennt** stillir þú reitinn **Vöruhús** á *51*.</span><span class="sxs-lookup"><span data-stu-id="174bf-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="174bf-220">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="174bf-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="174bf-221">Skráið hjá ykkur sölupöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="174bf-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="174bf-222">Bættu línu við nýju sölupöntunina og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="174bf-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="174bf-223">**Vörunúmer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="174bf-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="174bf-224">**Magn:** *20*</span><span class="sxs-lookup"><span data-stu-id="174bf-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="174bf-225">Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="174bf-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="174bf-226">Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá birgðirnar.</span><span class="sxs-lookup"><span data-stu-id="174bf-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="174bf-227">Lokaðu síðunni **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="174bf-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="174bf-228">Á aðgerðasvæðinu, á flipanum **Vöruhús**, skal velja **Losa í vöruhús** til að búa til vinnu fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="174bf-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="174bf-229">Þú færð upplýsingaboð sem sýna bylgjuauðkennið og sendingarauðkennin sem voru búin til fyrir sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="174bf-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="174bf-230">Sölupöntun 2</span><span class="sxs-lookup"><span data-stu-id="174bf-230">Sales order 2</span></span>

1. <span data-ttu-id="174bf-231">Í aðgerðarúðunni velurðu **Nýtt** til að búa til sölupöntun 2.</span><span class="sxs-lookup"><span data-stu-id="174bf-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="174bf-232">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="174bf-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="174bf-233">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="174bf-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="174bf-234">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="174bf-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="174bf-235">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="174bf-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="174bf-236">Skráið hjá ykkur sölupöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="174bf-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="174bf-237">Bættu línu við nýju sölupöntunina og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="174bf-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="174bf-238">**Vörunúmer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="174bf-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="174bf-239">**Magn:** *5*</span><span class="sxs-lookup"><span data-stu-id="174bf-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="174bf-240">Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="174bf-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="174bf-241">**Vörunúmer:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="174bf-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="174bf-242">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="174bf-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="174bf-243">Taka frá birgðir fyrir báðar línur.</span><span class="sxs-lookup"><span data-stu-id="174bf-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="174bf-244">Losa pöntun í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="174bf-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="174bf-245">Sölupöntun 3</span><span class="sxs-lookup"><span data-stu-id="174bf-245">Sales order 3</span></span>

1. <span data-ttu-id="174bf-246">Í aðgerðarúðunni velurðu **Nýtt** til að búa til sölupöntun 3.</span><span class="sxs-lookup"><span data-stu-id="174bf-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="174bf-247">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="174bf-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="174bf-248">**Viðskiptavinalykill:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="174bf-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="174bf-249">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="174bf-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="174bf-250">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="174bf-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="174bf-251">Skráið hjá ykkur sölupöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="174bf-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="174bf-252">Bættu línu við nýju sölupöntunina og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="174bf-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="174bf-253">**Vörunúmer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="174bf-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="174bf-254">**Magn:** *7*</span><span class="sxs-lookup"><span data-stu-id="174bf-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="174bf-255">Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="174bf-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="174bf-256">**Vörunúmer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="174bf-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="174bf-257">**Magn:** *8*</span><span class="sxs-lookup"><span data-stu-id="174bf-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="174bf-258">Taka frá birgðir fyrir báðar línur.</span><span class="sxs-lookup"><span data-stu-id="174bf-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="174bf-259">Losa pöntun í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="174bf-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="174bf-260">Sölupöntun 4</span><span class="sxs-lookup"><span data-stu-id="174bf-260">Sales order 4</span></span>

1. <span data-ttu-id="174bf-261">Í aðgerðarúðunni velurðu **Nýtt** til að búa til sölupöntun 4.</span><span class="sxs-lookup"><span data-stu-id="174bf-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="174bf-262">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="174bf-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="174bf-263">**Viðskiptavinalykill:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="174bf-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="174bf-264">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="174bf-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="174bf-265">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="174bf-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="174bf-266">Skráið hjá ykkur sölupöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="174bf-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="174bf-267">Bættu línu við nýju sölupöntunina og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="174bf-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="174bf-268">**Vörunúmer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="174bf-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="174bf-269">**Magn:** *25*</span><span class="sxs-lookup"><span data-stu-id="174bf-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="174bf-270">Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="174bf-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="174bf-271">**Vörunúmer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="174bf-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="174bf-272">**Magn:** *10*</span><span class="sxs-lookup"><span data-stu-id="174bf-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="174bf-273">Taka frá birgðir fyrir báðar línur.</span><span class="sxs-lookup"><span data-stu-id="174bf-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="174bf-274">Losa pöntun í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="174bf-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="174bf-275">Heimta vinnuauðkenni fyrir vinnuna sem var búin til</span><span class="sxs-lookup"><span data-stu-id="174bf-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="174bf-276">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="174bf-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="174bf-277">Sía á svæðinu **Vöruhús** þannig að aðeins vinna fyrir vöruhús *51* birtist.</span><span class="sxs-lookup"><span data-stu-id="174bf-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="174bf-278">Fjögur vinnuauðkenni ættu að vera búin til.</span><span class="sxs-lookup"><span data-stu-id="174bf-278">Four work IDs should have been created.</span></span> <span data-ttu-id="174bf-279">Skráið niður vinnuauðkenni hverrar sölupöntunar fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="174bf-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="174bf-280">Kenni sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="174bf-280">Sales order ID</span></span> | <span data-ttu-id="174bf-281">Vinnukenni</span><span class="sxs-lookup"><span data-stu-id="174bf-281">Work ID</span></span> | <span data-ttu-id="174bf-282">Vinnumagn</span><span class="sxs-lookup"><span data-stu-id="174bf-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="174bf-283">Sölupöntun 1</span><span class="sxs-lookup"><span data-stu-id="174bf-283">Sales Order 1</span></span> | <span data-ttu-id="174bf-284">Vinnuauðkenni 1</span><span class="sxs-lookup"><span data-stu-id="174bf-284">Work ID 1</span></span> | <span data-ttu-id="174bf-285">20 ea</span><span class="sxs-lookup"><span data-stu-id="174bf-285">20 ea</span></span> |
    | <span data-ttu-id="174bf-286">Sölupöntun 2</span><span class="sxs-lookup"><span data-stu-id="174bf-286">Sales Order 2</span></span> | <span data-ttu-id="174bf-287">Vinnuauðkenni 2</span><span class="sxs-lookup"><span data-stu-id="174bf-287">Work ID 2</span></span> | <span data-ttu-id="174bf-288">6 ea (summan af báðum línum)</span><span class="sxs-lookup"><span data-stu-id="174bf-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="174bf-289">Sölupöntun 3</span><span class="sxs-lookup"><span data-stu-id="174bf-289">Sales Order 3</span></span> | <span data-ttu-id="174bf-290">Vinnuauðkenni 3</span><span class="sxs-lookup"><span data-stu-id="174bf-290">Work ID 3</span></span> | <span data-ttu-id="174bf-291">15 ea (summan af báðum línum)</span><span class="sxs-lookup"><span data-stu-id="174bf-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="174bf-292">Sölupöntun 4</span><span class="sxs-lookup"><span data-stu-id="174bf-292">Sales Order 4</span></span> | <span data-ttu-id="174bf-293">Vinnuauðkenni 4</span><span class="sxs-lookup"><span data-stu-id="174bf-293">Work ID 4</span></span> | <span data-ttu-id="174bf-294">35 ea (summan af báðum línum)</span><span class="sxs-lookup"><span data-stu-id="174bf-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="174bf-295">Áður en þú keyrir flæðið í fartækið skaltu ganga úr skugga um að aðeins vinnan sem þú varst að búa til hafi stöðuna *Opin* fyrir vöruhús *51* og gerð verkbeiðni fyrir *Sölupöntun*.</span><span class="sxs-lookup"><span data-stu-id="174bf-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="174bf-296">Annars geta niðurstöður prófsins verið breytilegar, vegna þess kerfisstýrð tiltekt felur í sér alla tæka vinnu.</span><span class="sxs-lookup"><span data-stu-id="174bf-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="174bf-297">Opnaðu **Vöruhúsakerfi \> Vinna \> Á útleið \> Opin söluvinna**.</span><span class="sxs-lookup"><span data-stu-id="174bf-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="174bf-298">Í hnitanetinu **Opin söluvinna** síaðu svæðið **Vöruhús** þannig að aðeins vinna fyrir vöruhús *51* birtist.</span><span class="sxs-lookup"><span data-stu-id="174bf-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="174bf-299">Gakktu úr skugga um að aðeins birtist vinnuauðkennin fjögur sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="174bf-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="174bf-300">Lokaðu síðunni **Vinna**.</span><span class="sxs-lookup"><span data-stu-id="174bf-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="174bf-301">Framkvæmd flæðis í fartæki</span><span class="sxs-lookup"><span data-stu-id="174bf-301">Mobile device flow execution</span></span>

<span data-ttu-id="174bf-302">Miðað við uppsetninguna fæðir kerfið notanda vinnunni sem er raðað frá mesta magni vinnulínu til þeirrar lægstu.</span><span class="sxs-lookup"><span data-stu-id="174bf-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="174bf-303">Magnið á hverri línu verður minna en 20 ea.</span><span class="sxs-lookup"><span data-stu-id="174bf-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="174bf-304">Hafðu í huga að þessi uppsetning fangar alla vinnu sem hafa að minnsta kosti eina línu þar sem magnið er minna en 20 ea.</span><span class="sxs-lookup"><span data-stu-id="174bf-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="174bf-305">Þess vegna, ef verkið hefur aðra línu þar sem magnið er nákvæmlega 20 ea eða meira en 20 ea, mun það einnig gilda.</span><span class="sxs-lookup"><span data-stu-id="174bf-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="174bf-306">Fartækjaforrit</span><span class="sxs-lookup"><span data-stu-id="174bf-306">Mobile app</span></span>

1. <span data-ttu-id="174bf-307">Skráðu þig inn í vöruhúsaforritið sem notandi í vöruhúsi *51*.</span><span class="sxs-lookup"><span data-stu-id="174bf-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="174bf-308">Opnaðu **Á útleið \> Sölutiltekt - Kerfi**.</span><span class="sxs-lookup"><span data-stu-id="174bf-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="174bf-309">Tiltektarskrefið fyrir vinnuauðkenni *4* birtist.</span><span class="sxs-lookup"><span data-stu-id="174bf-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="174bf-310">Þetta vinnuauðkenni birtist fyrst vegna uppsetningarinnar á kerfisstýrðri fyrirspurnarpönun, þar sem þú tilgreindir að vinnan ætti að vera raðað miðað við lækkandi magn vinnulínu.</span><span class="sxs-lookup"><span data-stu-id="174bf-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="174bf-311">Ljúktu valinni tiltekt og frágangi til að loka vinnuauðkenninu.</span><span class="sxs-lookup"><span data-stu-id="174bf-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="174bf-312">Næst birtist vinnuauðkenni *3*.</span><span class="sxs-lookup"><span data-stu-id="174bf-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="174bf-313">Ein af vinnulínum hennar er næst í röðinni, byggð á magni vinnulínunnar.</span><span class="sxs-lookup"><span data-stu-id="174bf-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="174bf-314">Ljúktu tiltekt og frágangi til að loka vinnuauðkenninu.</span><span class="sxs-lookup"><span data-stu-id="174bf-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="174bf-315">Næst birtist vinnuauðkenni *2*.</span><span class="sxs-lookup"><span data-stu-id="174bf-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="174bf-316">Tiltektarlína þessarar vinnu er næst í röðinni.</span><span class="sxs-lookup"><span data-stu-id="174bf-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="174bf-317">Ljúktu tiltekt og frágangi til að loka vinnuauðkenninu.</span><span class="sxs-lookup"><span data-stu-id="174bf-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="174bf-318">Þú ættir ekki að sjá frekari vinnu birtast.</span><span class="sxs-lookup"><span data-stu-id="174bf-318">No further work should be presented to you.</span></span> <span data-ttu-id="174bf-319">Vinnuauðkenni *1* er ekki gjaldgengt fyrir þetta valmyndaratriði fartækis, því fyrirspurnin tilgreinir að vinnuhausar séu einungis taldir ef magn á vinnulínunum er minna en 20 ea.</span><span class="sxs-lookup"><span data-stu-id="174bf-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="174bf-320">Ábendingar</span><span class="sxs-lookup"><span data-stu-id="174bf-320">Tips</span></span>

<span data-ttu-id="174bf-321">Fyrirspurnir um kerfisstýrða vinnuröð eru *sameiginlegar*.</span><span class="sxs-lookup"><span data-stu-id="174bf-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="174bf-322">Mikilvægt er að þú hafir slíkt í huga við tilteknar uppsetningar.</span><span class="sxs-lookup"><span data-stu-id="174bf-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="174bf-323">Til dæmis viltu að tiltekinn valmyndaratriði vinni aðeins úr vinnu þar sem vinnueiningin er *ea*, og þú tilgreinir þá takmörkun á flipanum **Svið** á fyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="174bf-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="174bf-324">Í þessu tilfelli verður starfsmaðurinn mataður á allri vinnu þar sem að minnsta kosti ein vinnulína hefur vinnueininguna stillta á *ea*.</span><span class="sxs-lookup"><span data-stu-id="174bf-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="174bf-325">Þess vegna gæti þessi vinna einnig falið í sér vinnu þar sem vinnulínur eru með aðrar vinnueiningar en *ea* (eins og *kassa* eða *vörubretti*).</span><span class="sxs-lookup"><span data-stu-id="174bf-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="174bf-326">Fyrirspurnin útilokar eingöngu vinnu þar sem engin vinnulína hefur vinnueininguna stillt á *ea*.</span><span class="sxs-lookup"><span data-stu-id="174bf-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="174bf-327">Þess vegna, í dæminu við þessar aðstæður, var vinnuauðkenni *4* einnig fangað af fyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="174bf-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="174bf-328">Þegar það var búið var tveimur línum bætt við: ein fyrir 25 ea og önnur fyrir 10 ea.</span><span class="sxs-lookup"><span data-stu-id="174bf-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="174bf-329">Vinnan birtist notandanum samt sem áður, því að minnsta kosti ein vinnulína hefur minna magn en 20 ea.</span><span class="sxs-lookup"><span data-stu-id="174bf-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="174bf-330">Miðað við aðstæðurnar, getur þú komið í veg fyrir þessa aðgerð með því að nota vinnuhlé.</span><span class="sxs-lookup"><span data-stu-id="174bf-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]