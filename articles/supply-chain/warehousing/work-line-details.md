---
title: Upplýsingar um vinnulínu
description: Í þessu efnisatriði er að finna upplýsingar um upplýsingasíðu vinnulínu sem sýnir heildstæðan, raðanlegan og síanlegan lista yfir einstakar vinnulínur í kerfinu.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0cb182242a42443d5894b864523fc5f5fea9c5b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245107"
---
# <a name="work-line-details"></a><span data-ttu-id="6c292-103">Upplýsingar um vinnulínu</span><span class="sxs-lookup"><span data-stu-id="6c292-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c292-104">Síðan **Upplýsingar um vinnulínu** sýnir heildstæðan, raðanlegan og síanlegan lista yfir einstakar vinnulínur í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="6c292-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="6c292-105">Hún býður upp á heildaryfirlit yfir vinnu sem er verið að áætla og framkvæma í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="6c292-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="6c292-106">Auðvelt er að skipta á milli þess að skoða allar vinnulínur og skoða aðeins opnar vinnulínur.</span><span class="sxs-lookup"><span data-stu-id="6c292-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="6c292-107">Upplýsingar sem eru gefnar upp fyrir hverja línu innihalda verkstöðuna, vörunúmerið, staðsetningu, vinnumagn, farmkenni og sendingarkenni.</span><span class="sxs-lookup"><span data-stu-id="6c292-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="6c292-108">Kveikja á eiginleika vinnulínuupplýsinga</span><span class="sxs-lookup"><span data-stu-id="6c292-108">Turn on the work line details feature</span></span>

<span data-ttu-id="6c292-109">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="6c292-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="6c292-110">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="6c292-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6c292-111">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="6c292-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6c292-112">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="6c292-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6c292-113">**Heiti eiginleika:** *Upplýsingar um vinnulínu*</span><span class="sxs-lookup"><span data-stu-id="6c292-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="6c292-114">Opna og nota upplýsingasíðu vinnulínu</span><span class="sxs-lookup"><span data-stu-id="6c292-114">Open and use the Work line details page</span></span>

<span data-ttu-id="6c292-115">Til að skoða listann yfir upplýsingar um vinnulínur skal opna **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnulínu**.</span><span class="sxs-lookup"><span data-stu-id="6c292-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="6c292-116">Héðan er hægt að framkvæma eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="6c292-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="6c292-117">Notið reitinn **Sía** til að leita að línum sem eru með tiltekin gildi fyrir einhverja tiltæka færibreytu.</span><span class="sxs-lookup"><span data-stu-id="6c292-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="6c292-118">(Tiltækar færibreytur fela í sér margar færibreytur sem ekki eru sýndar sem dálkar í hnitanetinu.)</span><span class="sxs-lookup"><span data-stu-id="6c292-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="6c292-119">Notið gátreitinn **Sýna lokaðar** til að sýna eða fela lokaðar línur.</span><span class="sxs-lookup"><span data-stu-id="6c292-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="6c292-120">Veljið **Birta víddir** til að opna svargluggann **Birting vídda** þar sem hægt er að velja að sýna eða fela hina ýmsu dálka vídda í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="6c292-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="6c292-121">Veljið einhvern dálkahaus til að opna valmynd þar sem hægt er að velja um að raða eða sía listann eftir gildum í þeim dálki.</span><span class="sxs-lookup"><span data-stu-id="6c292-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="6c292-122">Veljið vinnulínu og veljið svo **Breyta staðsetningu** til að opna svarglugga þar sem hægt er að breyta staðsetningu þeirrar vinnulínu.</span><span class="sxs-lookup"><span data-stu-id="6c292-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="6c292-123">Staðsetningin sem tilgreind er mun hnekkja uppsetningu staðsetningarleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="6c292-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="6c292-124">Veljið vinnulínu og veljið svo **Hætta við vinnulínu** til að opna svarglugga þar sem hægt er að minnka magnið að hluta til eða að fullu fyrir þá vinnulínu.</span><span class="sxs-lookup"><span data-stu-id="6c292-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="6c292-125">Leiðréttið magn.</span><span class="sxs-lookup"><span data-stu-id="6c292-125">Adjust quantities.</span></span>
- <span data-ttu-id="6c292-126">Skoðið færslurnar á bak við hvaða vinnulínu sem er.</span><span class="sxs-lookup"><span data-stu-id="6c292-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="6c292-127">Prófa eiginleikann</span><span class="sxs-lookup"><span data-stu-id="6c292-127">Try out the feature</span></span>

<span data-ttu-id="6c292-128">Þessi hluti býður upp á sýniútgáfu í þremur hlutum sem sýnir hvernig á að vinna með upplýsingar vinnulínu.</span><span class="sxs-lookup"><span data-stu-id="6c292-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="6c292-129">Gera sýnigögn tiltæk</span><span class="sxs-lookup"><span data-stu-id="6c292-129">Make sample data available</span></span>

<span data-ttu-id="6c292-130">Til að vinna í gegnum þessa sýnikennslu með því að nota sýniskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="6c292-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="6c292-131">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="6c292-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="6c292-132">Einnig er hægt að nota þessa sýniútgáfu sem leiðsögn þegar unnið er í framleiðslukerfi.</span><span class="sxs-lookup"><span data-stu-id="6c292-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="6c292-133">Hinsvegar þarf að skipta út eigin gildum og einhverjar nauðsynlegar færslugerðir gæti vantað sem stöðluðu sýnigögnin bjóða upp á.</span><span class="sxs-lookup"><span data-stu-id="6c292-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="6c292-134">Staðfesta að uppsetning aðstæðna feli í sér nægar birgðir</span><span class="sxs-lookup"><span data-stu-id="6c292-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="6c292-135">Ef unnið er með sýnigögnin **USMF** ætti fyrst að ganga úr skugga um að kerfið sé sett upp þannig að nægar birgðir séu tiltækar á öllum viðeigandi tiltektarstaðsetningum.</span><span class="sxs-lookup"><span data-stu-id="6c292-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="6c292-136">Fyrir þessa sýniútgáfu er væntingin sú að eftirfarandi birgðir séu tiltækar:</span><span class="sxs-lookup"><span data-stu-id="6c292-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="6c292-137">**Atriði M9200:** 45 ea.</span><span class="sxs-lookup"><span data-stu-id="6c292-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="6c292-138">(eða fleiri)</span><span class="sxs-lookup"><span data-stu-id="6c292-138">(or more)</span></span>
- <span data-ttu-id="6c292-139">**Atriði M9202:** 10 ea.</span><span class="sxs-lookup"><span data-stu-id="6c292-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="6c292-140">(eða fleiri)</span><span class="sxs-lookup"><span data-stu-id="6c292-140">(or more)</span></span>

<span data-ttu-id="6c292-141">Fylgið þessum skrefum til að staðfesta að nægar birgðir séu til staðar og til að gera nauðsynlegar leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="6c292-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="6c292-142">Farið í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar** og ákveðið hvaða tiltektarstaðsetningar eru notaðar fyrir tiltekt sölupöntunar í vöruhúsi 51.</span><span class="sxs-lookup"><span data-stu-id="6c292-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="6c292-143">(Frekari upplýsingar er að finna í [Stýra vöruhúsavinnu með vinnusniðmátum og staðsetningarleiðbeiningum](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="6c292-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="6c292-144">Athugið birgðastöðu á staðsetningum sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="6c292-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="6c292-145">Leiðréttið birgðir eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="6c292-145">Adjust inventory as required.</span></span> <span data-ttu-id="6c292-146">Hægt er að búa til handvirkar hreyfingar, nota áfyllingu eða nota hvaða flæði sem er til að leiðrétta birgðirnar.</span><span class="sxs-lookup"><span data-stu-id="6c292-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="6c292-147">Hluti 1: Búa til tiltekt</span><span class="sxs-lookup"><span data-stu-id="6c292-147">Part 1: Create picking work</span></span>

<span data-ttu-id="6c292-148">Áður en hafist er handa við stofnun vinnu skal ganga úr skugga um vöruhúsið sé sett upp til að svara vinnubeiðnum á tilætlaðan hátt.</span><span class="sxs-lookup"><span data-stu-id="6c292-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="6c292-149">Fylgið þessum skrefum til að búa til tiltektarvinnu.</span><span class="sxs-lookup"><span data-stu-id="6c292-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="6c292-150">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="6c292-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6c292-151">Veljið **Ný** til að opna svargluggann **Stofna sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="6c292-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="6c292-152">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="6c292-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6c292-153">Á flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á _US-001_.</span><span class="sxs-lookup"><span data-stu-id="6c292-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="6c292-154">Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á _51_.</span><span class="sxs-lookup"><span data-stu-id="6c292-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="6c292-155">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="6c292-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="6c292-156">Nýja sölupöntunin þín opnast.</span><span class="sxs-lookup"><span data-stu-id="6c292-156">Your new sales order is opened.</span></span> <span data-ttu-id="6c292-157">Hún felur í sér nýja, auða línu í hnitanetinu **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="6c292-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="6c292-158">Í þessari pöntunarlínu skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="6c292-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="6c292-159">**Vörunúmer:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="6c292-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="6c292-160">**Magn:** _20_</span><span class="sxs-lookup"><span data-stu-id="6c292-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="6c292-161">**Prófhópur:** _ea_</span><span class="sxs-lookup"><span data-stu-id="6c292-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="6c292-162">Veljið nýju pöntunarlínuna og síðan í valmyndinni **Birgðir** skal velja **Frátekning** til að opna síðuna **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="6c292-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="6c292-163">Á síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="6c292-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="6c292-164">Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="6c292-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="6c292-165">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="6c292-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="6c292-166">Kerfið stofnar sendingu, bætir henni við nýja hleðslu og stofnar nauðsynlega vinnu.</span><span class="sxs-lookup"><span data-stu-id="6c292-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="6c292-167">Stofnið aðra sölupöntun fyrir sama viðskiptavinalykil og vöruhús sem notað var fyrir fyrstu pöntunina.</span><span class="sxs-lookup"><span data-stu-id="6c292-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="6c292-168">Bætið eftirfarandi tveimur pöntunarlínum við þessa pöntun:</span><span class="sxs-lookup"><span data-stu-id="6c292-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="6c292-169">**Lína 1:** Stillið reitinn **Vörunúmer** á _M9200_, reitinn **Magn** á _25_ og reitinn **Eining** á _ea_.</span><span class="sxs-lookup"><span data-stu-id="6c292-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="6c292-170">**Lína 2:** Stillið reitinn **Vörunúmer** á _M9202_, reitinn **Magn** á _10_ og reitinn **Eining** á _ea_.</span><span class="sxs-lookup"><span data-stu-id="6c292-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="6c292-171">Endurtakið skref 6 til 8 til að taka frá birgðir fyrir hverja pöntunarlínu (eina í einu) og endurtakið svo skref 9 til að losa pöntunina í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="6c292-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="6c292-172">Hluti 2: Breyta staðsetningu vinnulínu</span><span class="sxs-lookup"><span data-stu-id="6c292-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="6c292-173">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnulínu**.</span><span class="sxs-lookup"><span data-stu-id="6c292-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="6c292-174">Finnið og veljið eina af vinnulínunum sem stofnaðar voru fyrir þessa sýniútgáfu.</span><span class="sxs-lookup"><span data-stu-id="6c292-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="6c292-175">Veljið **Breyta staðsetningu** til að opna svargluggann **Velja nýja staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="6c292-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="6c292-176">Í svarglugganum **Velja nýja staðsetningu**, í reitnum **Staðsetning**, skal velja nýja staðsetningu fyrir vinnulínuna.</span><span class="sxs-lookup"><span data-stu-id="6c292-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="6c292-177">Velja skal **Í lagi** til að gera breytinguna og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="6c292-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c292-178">Aðeins er hægt að senda inn breytingar á staðsetningum ef nýja staðsetningin er með nægar birgðir tiltækar (fyrir tiltekt) eða ef hún kemst í gegnum staðfestingu staðsetningargerðar (fyrir frágang).</span><span class="sxs-lookup"><span data-stu-id="6c292-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="6c292-179">Hluti 3: Breyta magni vinnulínu eða hætta við vinnulínu</span><span class="sxs-lookup"><span data-stu-id="6c292-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="6c292-180">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnulínu**.</span><span class="sxs-lookup"><span data-stu-id="6c292-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="6c292-181">Finnið og veljið eina af vinnulínunum sem stofnaðar voru fyrir þessa sýniútgáfu.</span><span class="sxs-lookup"><span data-stu-id="6c292-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="6c292-182">Athugið að aðeins er hægt að hætta við eða breyta magni fyrir vinnulínur þar sem vinnugerðin er _tiltekt_.</span><span class="sxs-lookup"><span data-stu-id="6c292-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="6c292-183">Veljið **Hætta við vinnulínu** til að opna svargluggann **Magn sem á að hætta við**.</span><span class="sxs-lookup"><span data-stu-id="6c292-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="6c292-184">Í svarglugganum **Magn sem á að hætta við** skal breyta gildinu í reitnum **Magn** til að tiltaka magnið sem á að *draga frá* magninu sem tiltekið í línunni eins og er.</span><span class="sxs-lookup"><span data-stu-id="6c292-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="6c292-185">Sjálfgefið er að reiturinn **Magn** sýni fullt magn.</span><span class="sxs-lookup"><span data-stu-id="6c292-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="6c292-186">Ef hætt er við fullt magn verður gildinu **Staða verks** breytt í _Hætt við_, en reiturinn **Vinnumagn** sýnir áfram upprunalegt gildi.</span><span class="sxs-lookup"><span data-stu-id="6c292-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="6c292-187">Ef aðeins er hætt við hluta af magninu verður reiturinn **Vinnumagn** uppfærður til að sýna nýja magnið, en gildið **Staða verks** breytist ekki.</span><span class="sxs-lookup"><span data-stu-id="6c292-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="6c292-188">Velja skal **Í lagi** til að gera breytinguna og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="6c292-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c292-189">Ef aðeins er hætt við hluta af magninu fyrir vinnulínu þarf einnig að fjarlægja úrelt magn úr farmlínunni.</span><span class="sxs-lookup"><span data-stu-id="6c292-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="6c292-190">Að öðrum kosti, nema undirafhending sé sett upp á réttan hátt, er ekki hægt að staðfesta sendingu á farmlínu.</span><span class="sxs-lookup"><span data-stu-id="6c292-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]