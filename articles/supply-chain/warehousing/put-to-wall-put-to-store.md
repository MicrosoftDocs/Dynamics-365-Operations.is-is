---
title: Setja á vegg - setja í verslun
description: Þetta efnisatriði veitir upplýsingar um aðgerðina Setja á vegg - setja í verslun. Þessi virkni gerir þér kleift að takast á við atburðarásir þar sem þú verður að sameina vöru á biðsvæði forpökkunar, byggt á stillanlegu skilyrði. Hún hjálpar til við að draga úr tiltektartímanum vegna þess að hún gerir kleift að tína á eina marknúmeraplötu og getur notað fleiri frágangsstaðsetningar en klasatiltektir.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3f2ae63758fcb6247c5e56433645d9252576c755
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996276"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="4486d-105">Setja á vegg - setja í verslun</span><span class="sxs-lookup"><span data-stu-id="4486d-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4486d-106">Virknin *Setja á vegg - setja í verslun* gerir þér kleift að takast á við atburðarásir þar sem þú verður að sameina vöru á biðsvæði forpökkunar, byggt á stillanlegu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="4486d-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="4486d-107">Fyrst að þessi virkni gerir kleift að tína á eina marknúmeraplötu og getur notað fleiri frágangsstaðsetningar en klasatiltekt, munu fyrirtæki sem senda í verslanir eða meðhöndla litlar vörur hagnast á styttri tiltektartíma.</span><span class="sxs-lookup"><span data-stu-id="4486d-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="4486d-108">Verkflæðið fyrir þessa virkni beinir valdri vöru á röðunarstaðsetningu til að dreifa í ýmsar gerðir gáma.</span><span class="sxs-lookup"><span data-stu-id="4486d-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="4486d-109">Yfirleitt inniheldur hver röðunarstaðsetning margar röðunarstaði.</span><span class="sxs-lookup"><span data-stu-id="4486d-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="4486d-110">Hverjum röðunarstað er úthlutað samkvæmt skilyrðinu sem sett er af viðskiptaferlinu.</span><span class="sxs-lookup"><span data-stu-id="4486d-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="4486d-111">Dæmigerð skilyrði eru lokaáfangastaður, sending eða hleðsla.</span><span class="sxs-lookup"><span data-stu-id="4486d-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="4486d-112">Þegar vara kemur er henni dreift á hvern röðunarstað samkvæmt magninu sem tengist pöntuninni, áfangastaðnum, sendingunni eða hleðslunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="4486d-113">Þegar gámur er fullur eða honum lokið er hann fluttur á biðsvæði eða sendingarstað til frekari meðferðar, fer allt eftir viðskiptaferlinu.</span><span class="sxs-lookup"><span data-stu-id="4486d-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="4486d-114">Þessi vöruhúsaaðgerð er einnig kölluð öðrum nöfnum, t.d. „put-to-light“ og „break opens“.</span><span class="sxs-lookup"><span data-stu-id="4486d-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="4486d-115">Kveikja á eiginleika flokkunar á útleið</span><span class="sxs-lookup"><span data-stu-id="4486d-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="4486d-116">Áður en hægt er að nota virknina *Setja á vegg - setja í verslun*, verður að vera kveikt á eiginleikanum *Flokkun á útleið* í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="4486d-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="4486d-117">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="4486d-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="4486d-118">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="4486d-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="4486d-119">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="4486d-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4486d-120">**Heiti eiginleika:** *Flokkun á útleið*</span><span class="sxs-lookup"><span data-stu-id="4486d-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="4486d-121">Hægt er að nota eiginleikann *Flokkun á útleið* saman með eiginleikanum *Bylgjuskrefakóði fyrir allt fyrirtækið* ef kveikt er á honum.</span><span class="sxs-lookup"><span data-stu-id="4486d-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="4486d-122">Einnig þarf að kveikja á þessum eiginleika ef notaðir eru fyrirframskilgreindir kóðar sem settir eru upp í bylgjuskrefakóðum.</span><span class="sxs-lookup"><span data-stu-id="4486d-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="4486d-123">Í vinnusvæðinu **Stjórnun eiginleika** er þessi eiginleiki skráður á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="4486d-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="4486d-124">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="4486d-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4486d-125">**Heiti eiginleika:** *Stigskóði bylgju fyrir alla stofnunina/fyrirtækið*</span><span class="sxs-lookup"><span data-stu-id="4486d-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="4486d-126">Setja upp</span><span class="sxs-lookup"><span data-stu-id="4486d-126">Setup</span></span>

<span data-ttu-id="4486d-127">Í þessu sýnidæmi er venjuleg Contoso-gögn og vöruhús *62* notað.</span><span class="sxs-lookup"><span data-stu-id="4486d-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="4486d-128">Sumar viðbætur sem koma fram síðar eru einnig notaðar.</span><span class="sxs-lookup"><span data-stu-id="4486d-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="4486d-129">Staðsetningargerð</span><span class="sxs-lookup"><span data-stu-id="4486d-129">Location type</span></span>

1. <span data-ttu-id="4486d-130">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Gerðir staðsetninga**.</span><span class="sxs-lookup"><span data-stu-id="4486d-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="4486d-131">Á aðgerðasvæðinu skal velja **Ný** til að búa til staðsetningargerð fyrir röðun.</span><span class="sxs-lookup"><span data-stu-id="4486d-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="4486d-132">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-132">Set the following values:</span></span>

    - <span data-ttu-id="4486d-133">**Gerð staðsetningar:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="4486d-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="4486d-134">**Lýsing:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="4486d-135">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="4486d-136">Færibreytur vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="4486d-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="4486d-137">Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="4486d-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="4486d-138">Í flipanum **Almennt**, í flýtiflipanum **Gerðir staðsetninga**, í reitinn **Flokkun á gerð staðsetningar**, skal færa inn *SORT*.</span><span class="sxs-lookup"><span data-stu-id="4486d-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="4486d-139">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="4486d-140">Forstillingar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="4486d-140">Location profile</span></span>

1. <span data-ttu-id="4486d-141">Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="4486d-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="4486d-142">Veldu **Nýtt** á aðgerðasvæðinu til að búa til staðsetningarforstillingu fyrr flokkunarstaðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="4486d-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="4486d-143">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="4486d-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="4486d-144">**Kenni staðsetningarforstillingar:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="4486d-145">**Heiti:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="4486d-146">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="4486d-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4486d-147">**Staðsetningarsnið:** *PACK*</span><span class="sxs-lookup"><span data-stu-id="4486d-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="4486d-148">**Gerð staðsetningar:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="4486d-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="4486d-149">**Nota rakningu númeraplötu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="4486d-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="4486d-150">**Heimila blandaðar vörur:** *Já*</span><span class="sxs-lookup"><span data-stu-id="4486d-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="4486d-151">**Heimila blandaða birgðastöðu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="4486d-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="4486d-152">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="4486d-153">Staðsetningar</span><span class="sxs-lookup"><span data-stu-id="4486d-153">Locations</span></span>

1. <span data-ttu-id="4486d-154">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="4486d-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="4486d-155">Hreinsið gátreitinn **Mynda vartölur fyrir staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="4486d-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="4486d-156">Veldu **Nýtt** á aðgerðasvæðinu og stilltu svo eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="4486d-157">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="4486d-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="4486d-158">**Staðsetning:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="4486d-159">**Kenni staðsetningarforstillingar:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="4486d-160">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="4486d-161">Forstillingar umbúða</span><span class="sxs-lookup"><span data-stu-id="4486d-161">Packing profiles</span></span>

1. <span data-ttu-id="4486d-162">Fara í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Forstillingar umbúða**.</span><span class="sxs-lookup"><span data-stu-id="4486d-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="4486d-163">Veldu **Nýtt** á aðgerðasvæðinu og stilltu svo eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="4486d-164">**Forstillingarkenni pökkunar:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="4486d-165">**Lýsing:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="4486d-166">**Regla gámapökkunar:** Skiljið þennan reit eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="4486d-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="4486d-167">**Auðkennisstilling gáms:** *Sjálfvirkt*</span><span class="sxs-lookup"><span data-stu-id="4486d-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="4486d-168">**Gámagerð:** *PALLET 48x48*</span><span class="sxs-lookup"><span data-stu-id="4486d-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="4486d-169">**Stofna gám sjálfkrafa þegar gámi er lokað:** Skiljið þennan reit eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="4486d-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="4486d-170">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="4486d-171">Kóðar bylgjuskrefs</span><span class="sxs-lookup"><span data-stu-id="4486d-171">Wave step codes</span></span>

<span data-ttu-id="4486d-172">Ef kveikt var á eiginleikanum *Bylgjuskrefakóði fyrir allt fyrirtækið* skal setja upp eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="4486d-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="4486d-173">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**.</span><span class="sxs-lookup"><span data-stu-id="4486d-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="4486d-174">Veldu **Nýtt** á aðgerðasvæðinu og stilltu svo eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="4486d-175">**Kóði bylgjuskrefs:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="4486d-176">**Lýsing á bylgjuskrefi:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="4486d-177">**Gerð bylgjuskrefs:** *Sniðmát flokkunar*</span><span class="sxs-lookup"><span data-stu-id="4486d-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="4486d-178">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="4486d-179">Sniðmát flokkunar á útleið</span><span class="sxs-lookup"><span data-stu-id="4486d-179">Outbound sorting template</span></span>

<span data-ttu-id="4486d-180">Flokkunarsniðmátið stjórnar því hvort röðunarstaðir eru búnir til, hvaða skilyrði eru notuð og aðrar eigindir röðunarferlisins.</span><span class="sxs-lookup"><span data-stu-id="4486d-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="4486d-181">Farið í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Flokkunarsniðmát á útleið**.</span><span class="sxs-lookup"><span data-stu-id="4486d-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="4486d-182">Á aðgerðasvæðinu skal velja **Nýtt** til að búa flokkunarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="4486d-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="4486d-183">Stilltu eftirfarandi gildi í haus nýja sniðmátsins:</span><span class="sxs-lookup"><span data-stu-id="4486d-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="4486d-184">**Kenni fyrir flokkunarsniðmát á útleið:** *Bylgjuröðun*</span><span class="sxs-lookup"><span data-stu-id="4486d-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="4486d-185">**Lýsing:** *Bylgjuröðun*</span><span class="sxs-lookup"><span data-stu-id="4486d-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="4486d-186">**Sniðmátsgerð röðunar:** *Bylgjueftirspurn*</span><span class="sxs-lookup"><span data-stu-id="4486d-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="4486d-187">Þessi reitur skilgreinir ferlið sem flokkunarsniðmátið er notað í.</span><span class="sxs-lookup"><span data-stu-id="4486d-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="4486d-188">Eftirtalin gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="4486d-188">The following values are available:</span></span>

        - <span data-ttu-id="4486d-189">**Bylgjueftirspurn** - Flokkunarsniðmátið er notað fyrir ferlið *Setja á vegg*.</span><span class="sxs-lookup"><span data-stu-id="4486d-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="4486d-190">Þessi sniðmátsgerð er notuð til að komast framhjá pökkunarstöðinni og vinna úr birgðum beint úr bylgjunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="4486d-191">Þú getur aðeins notað þessa gerð ef bylgjuúrvinnsluaðferðin **röðun** er höfð með í bylgjusniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="4486d-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="4486d-192">**Gámur** - Flokkunarsniðmátið er notað fyrir ferlið *Röðun á bretti eftir pökkun*.</span><span class="sxs-lookup"><span data-stu-id="4486d-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="4486d-193">Þessi sniðmátsgerð er notuð við úrvinnslu á gámum sem eru lokaðir á pökkunarstöðinni og sem þarf að raða á bretti.</span><span class="sxs-lookup"><span data-stu-id="4486d-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="4486d-194">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="4486d-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="4486d-195">**Staðsetning:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="4486d-196">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="4486d-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4486d-197">**Sannprófun röðunar:** *Skönnun stöðu*</span><span class="sxs-lookup"><span data-stu-id="4486d-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="4486d-198">Þessi reitur skilgreinir sannprófunina sem krafist er við röðunina.</span><span class="sxs-lookup"><span data-stu-id="4486d-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="4486d-199">Eftirtalin gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="4486d-199">The following values are available:</span></span>

        - <span data-ttu-id="4486d-200">Engum</span><span class="sxs-lookup"><span data-stu-id="4486d-200">None</span></span>
        - <span data-ttu-id="4486d-201">Skönnun númeraplötu</span><span class="sxs-lookup"><span data-stu-id="4486d-201">License plate scan</span></span>
        - <span data-ttu-id="4486d-202">Skönnun stöðu</span><span class="sxs-lookup"><span data-stu-id="4486d-202">Position scan</span></span>

    - <span data-ttu-id="4486d-203">**Stofna vinnu á lokun stöðu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="4486d-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="4486d-204">Ef þessi valkostur er stilltur á *Já*, þegar staðan er lokuð, verður vinna stofnuð til að færa birgðir á lokasendingarstaðinn.</span><span class="sxs-lookup"><span data-stu-id="4486d-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="4486d-205">Ef hann er stilltur á *Nei* verða birgðir strax tíndar fyrir pöntunina þegar staðan er lokuð.</span><span class="sxs-lookup"><span data-stu-id="4486d-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="4486d-206">**Stöðuverkefni:** *Handvirkt*</span><span class="sxs-lookup"><span data-stu-id="4486d-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="4486d-207">Þessi reitur skilgreinir gerð af úthlutun staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="4486d-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="4486d-208">Eftirtalin gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="4486d-208">The following values are available:</span></span>

        - <span data-ttu-id="4486d-209">**Handvirkt** - notandi verður alltaf að tilgreina hvaða stöðu birgðir eiga að vera flokkaðar í.</span><span class="sxs-lookup"><span data-stu-id="4486d-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="4486d-210">**Sjálfvirkt** - kerfið beinir birgðum sjálfkrafa að stöðu þegar það er í boði, á grunni sundurliðana sniðmátsflokkunar.</span><span class="sxs-lookup"><span data-stu-id="4486d-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="4486d-211">**Úthluta skilyrði röðunarstaðs:** *Aðeins nota tóma staði*</span><span class="sxs-lookup"><span data-stu-id="4486d-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="4486d-212">Þessi reitur stjórnar því hvort tekið er tillit til birgða sem þegar eru til staðar á röðunarstaðnum þegar stað er úthlutað fyrir eftirspurnina.</span><span class="sxs-lookup"><span data-stu-id="4486d-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="4486d-213">Eftirtalin gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="4486d-213">The following values are available:</span></span>

        - <span data-ttu-id="4486d-214">**Aðeins nota tóman stað** - Staðir sem þegar eru með birgðir sem tengjast þeim verða teknir til greina</span><span class="sxs-lookup"><span data-stu-id="4486d-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="4486d-215">**Gert er ráð fyrir auðri staðsetningu** - Litið verður framhjá öllum birgðum sem eru á staðnum við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="4486d-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="4486d-216">Allar lausar stöður verða notaðar.</span><span class="sxs-lookup"><span data-stu-id="4486d-216">All available positions will be used.</span></span>

    - <span data-ttu-id="4486d-217">**Kóði bylgjuskrefs:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="4486d-218">Ef kveikt er á eiginleikanum *Bylgjuskrefakóði fyrir allt fyrirtækið* verður einnig setja upp bylgjuskrefakóðann *Raða* í bylgjuskrefakóðum.</span><span class="sxs-lookup"><span data-stu-id="4486d-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="4486d-219">**Loka sjálfkrafa röðun staðsetningar:** *Já*</span><span class="sxs-lookup"><span data-stu-id="4486d-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="4486d-220">Ef þessi valkostur er stilltur á *Já* verður röðunarstaðnum sjálfkrafa lokað þegar allri vinnu sem kemur á staðinn hefur verið lokið.</span><span class="sxs-lookup"><span data-stu-id="4486d-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="4486d-221">**Fjöldi flokkaðra staðsetninga:** *3*</span><span class="sxs-lookup"><span data-stu-id="4486d-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="4486d-222">Þessi reitur skilgreinir hámarksfjölda röðunarstaða sem kerfið mun búa til.</span><span class="sxs-lookup"><span data-stu-id="4486d-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="4486d-223">**Forskeyti fyrir röðun staðsetningar:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="4486d-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="4486d-224">Þessi reitur skilgreinir forskeytið sem kerfið úthlutar á undan númeri staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="4486d-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="4486d-225">**Pakka sjálfkrafa röðun staðsetningar:** *Já*</span><span class="sxs-lookup"><span data-stu-id="4486d-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="4486d-226">Ef þessi valkostur er stilltur á *Já* verða birgðirnar á röðunarstaðnum pakkaðar í gám þegar staðsetningunni er lokað.</span><span class="sxs-lookup"><span data-stu-id="4486d-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="4486d-227">**Forstillingarkenni pökkunar:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="4486d-228">Þessi reitur skilgreinir pökkunarforstillinguna sem verður notuð þegar röðunarstaðnum er pakkað í gám.</span><span class="sxs-lookup"><span data-stu-id="4486d-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="4486d-229">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að tilgreina skilyrðið sem notað er fyrir þetta flokkunarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="4486d-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="4486d-230">Í svarglugga fyrirspurnar, í flipanum **Röðun**, skal velja **Ný** til að bæta við línu og síðan stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="4486d-231">**Tafla:** *Upplýsingar um hleðslu*</span><span class="sxs-lookup"><span data-stu-id="4486d-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="4486d-232">**Afleidd tafla:** *Upplýsingar um hleðslu*</span><span class="sxs-lookup"><span data-stu-id="4486d-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="4486d-233">**Reitur:** *Auðkenni sendingar*</span><span class="sxs-lookup"><span data-stu-id="4486d-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="4486d-234">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="4486d-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="4486d-235">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4486d-235">Select **OK**.</span></span>
1. <span data-ttu-id="4486d-236">Þú gætir fengið eftirfarandi skilaboð: „Flokkun verður endurstillt, á að halda áfram?"</span><span class="sxs-lookup"><span data-stu-id="4486d-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="4486d-237">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="4486d-237">Select **Yes**.</span></span>

    <span data-ttu-id="4486d-238">Hnappur **Sundurliðanir flokkunarsniðmáts á útleið** á aðgerðasvæðinu verður tiltækur.</span><span class="sxs-lookup"><span data-stu-id="4486d-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="4486d-239">Á aðgerðasvæðinu skal velja **Sundurliðanir flokkunarsniðmáts á útleið**.</span><span class="sxs-lookup"><span data-stu-id="4486d-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="4486d-240">Veljið gátreitinn **Flokka eftir reit** til að flokka eftir auðkenni sendingar.</span><span class="sxs-lookup"><span data-stu-id="4486d-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="4486d-241">Þessi stilling býr til eina röðunarstaðsetningu á hverja sendingu sem er gámur í bylgjunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="4486d-242">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4486d-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="4486d-243">Vinnsluaðferðir bylgju</span><span class="sxs-lookup"><span data-stu-id="4486d-243">Wave process methods</span></span>

1. <span data-ttu-id="4486d-244">Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.</span><span class="sxs-lookup"><span data-stu-id="4486d-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="4486d-245">Veldu **Endurgera aðferðir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="4486d-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="4486d-246">Aðferð **röðunar** er bætt við listann yfir tiltækar aðferðir og bylgjusniðmátsgerðin *Sending* er valin fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="4486d-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="4486d-247">Bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="4486d-247">Wave templates</span></span>

<span data-ttu-id="4486d-248">Breytið bylgjusniðmátinu sem notað er fyrir röðun bylgjueftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="4486d-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="4486d-249">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="4486d-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="4486d-250">Í reitnum **Bylgjusniðmátsgerð** skal velja *Sending*.</span><span class="sxs-lookup"><span data-stu-id="4486d-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="4486d-251">Veljið fyrirliggjandi sniðmát **62 Sjálfgefin sending**.</span><span class="sxs-lookup"><span data-stu-id="4486d-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="4486d-252">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="4486d-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4486d-253">Í flýtiflipanum **Almennt** skal gera eftirfarandi breytingar:</span><span class="sxs-lookup"><span data-stu-id="4486d-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="4486d-254">Stilla valkostinn fyrir **Vinna úr bylgju við losun í vörugeymslu** á *Nei*.</span><span class="sxs-lookup"><span data-stu-id="4486d-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="4486d-255">Stilla valkostinn **Úthluta** á opnar bylgjur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="4486d-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="4486d-256">Í flýtiflipanum **Aðferðir** skal setja upp aðferðina **röðun**:</span><span class="sxs-lookup"><span data-stu-id="4486d-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="4486d-257">Í hnitanetinu **Eftirstandandi aðferðir** skal velja **röðun**.</span><span class="sxs-lookup"><span data-stu-id="4486d-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="4486d-258">Veljið hægri örvarhnappinn til að færa **röðun** yfir á hnitanetið **Valdar aðferðir**.</span><span class="sxs-lookup"><span data-stu-id="4486d-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="4486d-259">Í hnitanetinu **Valdar aðferðir** skal velja **röðun**.</span><span class="sxs-lookup"><span data-stu-id="4486d-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="4486d-260">Stillið reitinn **Bylgjuskrefakóði** á *Raða*.</span><span class="sxs-lookup"><span data-stu-id="4486d-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="4486d-261">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="4486d-262">Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="4486d-262">Mobile device menu items</span></span>

1. <span data-ttu-id="4486d-263">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="4486d-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="4486d-264">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4486d-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4486d-265">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="4486d-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="4486d-266">**Heiti valmyndaratriðis:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="4486d-267">**Titill:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="4486d-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="4486d-268">**Stilling:** *Óbein*</span><span class="sxs-lookup"><span data-stu-id="4486d-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="4486d-269">**Nota fyrirliggjandi vinnu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="4486d-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="4486d-270">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="4486d-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4486d-271">**Verkþáttarkóði:** *Röðun á útleið*</span><span class="sxs-lookup"><span data-stu-id="4486d-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="4486d-272">**Nota leiðbeiningar fyrir ferli:** *Já* (sjálfgefið gildi)</span><span class="sxs-lookup"><span data-stu-id="4486d-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="4486d-273">**Kenni fyrir flokkunarsniðmát á útleið:** *Bylgjuröðun*</span><span class="sxs-lookup"><span data-stu-id="4486d-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="4486d-274">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="4486d-275">Valmynd fartækis</span><span class="sxs-lookup"><span data-stu-id="4486d-275">Mobile device menu</span></span>

1. <span data-ttu-id="4486d-276">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="4486d-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="4486d-277">Veldu **Á útleið** á valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="4486d-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="4486d-278">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="4486d-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4486d-279">Í hnitanetinu **Tiltækar valmyndir og valmyndaratriði** skal finna og velja valmyndaratriðið **Raða** sem var verið að búa til.</span><span class="sxs-lookup"><span data-stu-id="4486d-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="4486d-280">Smellið á hægri örvarhnappinn til að færa **Raða** yfir á hnitanetið **Valmyndarskipan**.</span><span class="sxs-lookup"><span data-stu-id="4486d-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="4486d-281">Á þennan hátt er valmyndaratriðinu bætt við valmyndina **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="4486d-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="4486d-282">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="4486d-283">Staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="4486d-283">Location directives</span></span>

<span data-ttu-id="4486d-284">Búa þarf til staðsetningarleiðbeiningar til að leiða áfram vinnuna sem búin er til eftir að röðuninni lýkur.</span><span class="sxs-lookup"><span data-stu-id="4486d-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="4486d-285">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="4486d-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="4486d-286">Í reitnum **Gerð verkbeiðni** skal velja *Röðuð birgðatínsla*.</span><span class="sxs-lookup"><span data-stu-id="4486d-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="4486d-287">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4486d-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4486d-288">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="4486d-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="4486d-289">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="4486d-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="4486d-290">**Heiti:** *Koma fyrir í útskoti*</span><span class="sxs-lookup"><span data-stu-id="4486d-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="4486d-291">Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**:</span><span class="sxs-lookup"><span data-stu-id="4486d-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4486d-292">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="4486d-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="4486d-293">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="4486d-293">**Site:** *6*</span></span>
    - <span data-ttu-id="4486d-294">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="4486d-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="4486d-295">**Leiðbeiningarkóði:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="4486d-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="4486d-296">**Margar birgðahaldseiningar:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="4486d-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="4486d-297">Veldu **Vista** til að gera flýtiflipann **Línur** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="4486d-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="4486d-298">Í flýtiflipanum **Línur** skal velja **Ný** og stilla síðan eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="4486d-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="4486d-299">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="4486d-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="4486d-300">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="4486d-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4486d-301">**Frá-magn:** *0*</span><span class="sxs-lookup"><span data-stu-id="4486d-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="4486d-302">**Til magn:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="4486d-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="4486d-303">Veldu **Vista** til að gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="4486d-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="4486d-304">Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Ný** og stilla síðan eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="4486d-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="4486d-305">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="4486d-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="4486d-306">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="4486d-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4486d-307">**Heiti:** *Útskot*</span><span class="sxs-lookup"><span data-stu-id="4486d-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="4486d-308">Veldu **Vista** til að gera hnappinn **Breyta fyrirspurn** á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum**.</span><span class="sxs-lookup"><span data-stu-id="4486d-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="4486d-309">Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="4486d-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="4486d-310">Í svarglugga fyrirspurnarritilsins, í flipanum **Svið**, skal finna línuna þar sem reiturinn **Svæði** er stilltur á *Staðsetning*.</span><span class="sxs-lookup"><span data-stu-id="4486d-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="4486d-311">Stillið reitinn **Skilyrði** fyrir þessa línu á *Útskot*.</span><span class="sxs-lookup"><span data-stu-id="4486d-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="4486d-312">Smellið á **Í lagi** til að staðfesta breytinguna.</span><span class="sxs-lookup"><span data-stu-id="4486d-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="4486d-313">Vinnuklasar</span><span class="sxs-lookup"><span data-stu-id="4486d-313">Work classes</span></span>

1. <span data-ttu-id="4486d-314">Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.</span><span class="sxs-lookup"><span data-stu-id="4486d-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="4486d-315">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4486d-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4486d-316">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="4486d-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="4486d-317">**Auðkenni vinnuklasa:** *Röðun*</span><span class="sxs-lookup"><span data-stu-id="4486d-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="4486d-318">**Lýsing:** *Röðun*</span><span class="sxs-lookup"><span data-stu-id="4486d-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="4486d-319">**Gerð verkbeiðni:** *Röðuð birgðatínsla*</span><span class="sxs-lookup"><span data-stu-id="4486d-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="4486d-320">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="4486d-321">Vinnusniðmát</span><span class="sxs-lookup"><span data-stu-id="4486d-321">Work templates</span></span>

1. <span data-ttu-id="4486d-322">Opnaðu **Vöruhúsastjórnun \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="4486d-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="4486d-323">Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="4486d-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="4486d-324">Í hnitanetinu skal velja vinnusniðmátið **62 Tína til að pakka**.</span><span class="sxs-lookup"><span data-stu-id="4486d-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="4486d-325">Á aðgerðasvæðinu skal velja **Vinnuhausaskil**.</span><span class="sxs-lookup"><span data-stu-id="4486d-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="4486d-326">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="4486d-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4486d-327">Í línunni þar sem reiturinn **Heiti svæðis** er stillt á *Auðkenni sendingar* skal hreinsa gátreitinn **Flokka eftir þessum reit**.</span><span class="sxs-lookup"><span data-stu-id="4486d-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="4486d-328">Veljið **Vista** og lokið síðan svarglugganum **Vinnuhausaskil**.</span><span class="sxs-lookup"><span data-stu-id="4486d-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="4486d-329">Í reitnum **Gerð verkbeiðni** skal velja *Röðuð birgðatínsla*.</span><span class="sxs-lookup"><span data-stu-id="4486d-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="4486d-330">Veljið **Nýtt** til að búa til vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="4486d-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="4486d-331">Í hlutanum **Yfirlit** skal stilla eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="4486d-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="4486d-332">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="4486d-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="4486d-333">**Vinnusniðmát:** *Röðuð tiltekt*</span><span class="sxs-lookup"><span data-stu-id="4486d-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="4486d-334">**Lýsing á vinnusniðmáti:** *Röðuð tiltekt*</span><span class="sxs-lookup"><span data-stu-id="4486d-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="4486d-335">Veljið **Vista** til að gera hlutann **Upplýsingar um vinnusniðmát** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="4486d-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="4486d-336">Í hlutanum **Upplýsingar vinnusniðmáts** býrðu til tvær línur.</span><span class="sxs-lookup"><span data-stu-id="4486d-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="4486d-337">Veldu **Nýtt** og stilltu síðan eftirfarandi gildi fyrir línu 1:</span><span class="sxs-lookup"><span data-stu-id="4486d-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="4486d-338">**Verkgerð:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="4486d-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="4486d-339">**Áskilið:** Valið (= *Já*)</span><span class="sxs-lookup"><span data-stu-id="4486d-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="4486d-340">**Auðkenni vinnuklasa:** *Röðun*</span><span class="sxs-lookup"><span data-stu-id="4486d-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="4486d-341">Veljið aftur **Ný** og stillið síðan eftirfarandi gildi fyrir línu 2:</span><span class="sxs-lookup"><span data-stu-id="4486d-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="4486d-342">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="4486d-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="4486d-343">**Áskilið:** Valið (= *Já*)</span><span class="sxs-lookup"><span data-stu-id="4486d-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="4486d-344">**Auðkenni vinnuklasa:** *Röðun*</span><span class="sxs-lookup"><span data-stu-id="4486d-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="4486d-345">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="4486d-346">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4486d-346">Example scenario</span></span>

<span data-ttu-id="4486d-347">Þessi atburðarás líkir eftir aðstæðum þar sem vöruhúsið geymir litlar vörur í staðsetningum og verður að pakka þeim í kassa áður en þær eru sendar, og þar sem virkni pökkunarstöðva hentar í raun ekki.</span><span class="sxs-lookup"><span data-stu-id="4486d-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="4486d-348">Starfsmenn tína pantanir fyrir marga viðskiptavini og mismunandi heimilisföng á sama tíma til að auka tínsluhraðann.</span><span class="sxs-lookup"><span data-stu-id="4486d-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="4486d-349">Eftir að tínslu lýkur fara starfsmenn á röðunarstaðsetninguna þar sem hægt er að flokka tíndar vörur í réttan kassa samkvæmt áskildum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="4486d-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="4486d-350">Í þessu dæmi verður auðkenni sendingarinnar notað til að ákvarða réttan kassa vegna þess að hver sending er með sitt eigið heimilisfang.</span><span class="sxs-lookup"><span data-stu-id="4486d-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="4486d-351">Þegar búið er að pakka og raða öllum vörum hleðslunnar eftir sendingu, verða kassarnir færðir yfir á biðsvæðið og að lokum hlaðnir inn í flutningabíl.</span><span class="sxs-lookup"><span data-stu-id="4486d-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="4486d-352">Áður en hafist er handa með atburðarásina skal ganga úr skugga um að allar venjulegar vöruhúsaaðgerðir séu settar upp á réttan hátt fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="4486d-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="4486d-353">Hefðbundið Contoso-vöruhús *62* er notað í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="4486d-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="4486d-354">Hefðbundnum skilgreiningum hefur ekki verið breytt, fyrir utan því sem lýst er í uppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="4486d-355">Búa til eftirspurn</span><span class="sxs-lookup"><span data-stu-id="4486d-355">Create demand</span></span>

<span data-ttu-id="4486d-356">Áður en hægt er að sýna virknina þarf að búa til eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="4486d-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="4486d-357">Í þessari atburðarás býrðu til þrjár sölupantanir fyrir þrjá mismunandi viðskiptavini til að líkja eftir mismunandi afhendingaraðsetrum.</span><span class="sxs-lookup"><span data-stu-id="4486d-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="4486d-358">Þú býrð þar af leiðandi til þrjár aðskildar sendingar.</span><span class="sxs-lookup"><span data-stu-id="4486d-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="4486d-359">Áður en þú stofnar sölupantanir og sendingar skaltu ganga úr skugga um að tiltektarstaðsetningar hafi nægar birgðir fyrir allar vörurnar í pöntunum.</span><span class="sxs-lookup"><span data-stu-id="4486d-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="4486d-360">Farið yfir stillingar staðsetningarleiðbeiningarinnar til að staðfesta tiltektarstaðsetningarnar sem notaðar eru fyrir tiltekt sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="4486d-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="4486d-361">Ef þú verður að breyta birgðum geturðu búið til handvirkar birgðahreyfingar, notað áfyllingu eða notað hvaða annað flæði sem er.</span><span class="sxs-lookup"><span data-stu-id="4486d-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="4486d-362">Því næst taka frá birgðirnar.</span><span class="sxs-lookup"><span data-stu-id="4486d-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="4486d-363">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="4486d-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4486d-364">Veljið **Ný** til að stofna sölupöntun fyrir pöntun 1.</span><span class="sxs-lookup"><span data-stu-id="4486d-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="4486d-365">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="4486d-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4486d-366">**Viðskiptavinur:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4486d-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="4486d-367">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="4486d-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="4486d-368">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4486d-368">Select **OK**.</span></span>
1. <span data-ttu-id="4486d-369">Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="4486d-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4486d-370">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-370">Set the following values:</span></span>

    - <span data-ttu-id="4486d-371">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4486d-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4486d-372">**Magn:** *5*</span><span class="sxs-lookup"><span data-stu-id="4486d-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="4486d-373">Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="4486d-374">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="4486d-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="4486d-375">**Magn:** *10*</span><span class="sxs-lookup"><span data-stu-id="4486d-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="4486d-376">Endurtakið eftirfarandi skref fyrir hverja sölulínu í pöntuninni til að taka frá birgðir fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="4486d-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="4486d-377">Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Birgðir** velur þú **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="4486d-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="4486d-378">Á síðunni **Frátekning** skal velja **Frátektarlota** og loka svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="4486d-379">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-379">Select **Save**.</span></span>

1. <span data-ttu-id="4486d-380">Veljið **Ný** til að stofna sölupöntun fyrir pöntun 2.</span><span class="sxs-lookup"><span data-stu-id="4486d-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="4486d-381">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="4486d-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4486d-382">**Viðskiptavinur:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="4486d-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="4486d-383">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="4486d-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="4486d-384">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4486d-384">Select **OK**.</span></span>
1. <span data-ttu-id="4486d-385">Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="4486d-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4486d-386">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-386">Set the following values:</span></span>

    - <span data-ttu-id="4486d-387">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4486d-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4486d-388">**Magn:** *7*</span><span class="sxs-lookup"><span data-stu-id="4486d-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="4486d-389">Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="4486d-390">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="4486d-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="4486d-391">**Magn:** *3*</span><span class="sxs-lookup"><span data-stu-id="4486d-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="4486d-392">Endurtakið eftirfarandi skref fyrir hverja sölulínu í pöntuninni til að taka frá birgðir fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="4486d-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="4486d-393">Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Birgðir** velur þú **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="4486d-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="4486d-394">Á síðunni **Frátekning** skal velja **Frátektarlota** og loka svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="4486d-395">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-395">Select **Save**.</span></span>

1. <span data-ttu-id="4486d-396">Veljið **Ný** til að stofna sölupöntun fyrir pöntun 3.</span><span class="sxs-lookup"><span data-stu-id="4486d-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="4486d-397">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="4486d-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4486d-398">**Viðskiptavinur:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="4486d-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="4486d-399">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="4486d-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="4486d-400">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4486d-400">Select **OK**.</span></span>
1. <span data-ttu-id="4486d-401">Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="4486d-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4486d-402">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="4486d-402">Set the following values:</span></span>

    - <span data-ttu-id="4486d-403">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4486d-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4486d-404">**Magn:** *8*</span><span class="sxs-lookup"><span data-stu-id="4486d-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="4486d-405">Fylgið þessum skrefum til að taka frá birgðir fyrir sölulínuna:</span><span class="sxs-lookup"><span data-stu-id="4486d-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="4486d-406">Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Birgðir** velur þú **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="4486d-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="4486d-407">Á síðunni **Frátekning** skal velja **Frátektarlota** og loka svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="4486d-408">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4486d-408">Select **Save**.</span></span>

<span data-ttu-id="4486d-409">Ljúkið við eftirfarandi ferli til að losa hverja sölupöntun fyrir sig í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="4486d-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="4486d-410">Þrjár mismunandi sendingar verða búnar til.</span><span class="sxs-lookup"><span data-stu-id="4486d-410">Three different shipments will be created.</span></span> <span data-ttu-id="4486d-411">Þú bætir síðan öllum þremur sendingunum við nýja bylgju.</span><span class="sxs-lookup"><span data-stu-id="4486d-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="4486d-412">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="4486d-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4486d-413">Í hnitanetinu skal velja fyrstu sölupöntunina sem var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="4486d-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="4486d-414">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="4486d-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4486d-415">Þú færð skilaboð með upplýsingum um bylgjuauðkenni og sendingarkenni sem voru búin til.</span><span class="sxs-lookup"><span data-stu-id="4486d-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="4486d-416">Endurtaktu fyrri skrefin til að losa sölupantanir 2 og 3 í vöruhús.</span><span class="sxs-lookup"><span data-stu-id="4486d-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="4486d-417">Takið eftir að upplýsingarnar í skilaboðunum sem birtust tilgreina að sendingu hafi verið bætt við bylgjuna sem var búin til þegar sölupöntun 1 var losuð.</span><span class="sxs-lookup"><span data-stu-id="4486d-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="4486d-418">Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="4486d-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="4486d-419">Veljið bylgjukennið sem var búið til úr losuninni á sölupöntuninni til að opna síðuna **Bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="4486d-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="4486d-420">Þessi síða sýnir upplýsingar um bylgjuna.</span><span class="sxs-lookup"><span data-stu-id="4486d-420">This page shows the wave details.</span></span> <span data-ttu-id="4486d-421">Flýtiflipinn **Bylgjulínur** sýnir sendingarnar sem búnar voru til.</span><span class="sxs-lookup"><span data-stu-id="4486d-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="4486d-422">Nú þarf að búa til vinnu til að fara með vörur af tiltektarstaðsetningum og yfir á röðunarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4486d-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="4486d-423">Á aðgerðasvæðinu skal velja **Úrvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="4486d-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="4486d-424">Við bylgjuvinnslu mun flokkunaraðferðin nota flokkunarsniðmátið til að úthluta birgðum á röðunarstaði.</span><span class="sxs-lookup"><span data-stu-id="4486d-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="4486d-425">Þegar bylgjuvinnslu er lokið færðu skilaboð með upplýsingum um að bylgjan hafi verið bókuð vinna hafi verið búin til.</span><span class="sxs-lookup"><span data-stu-id="4486d-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="4486d-426">Á Aðgerðasvæðinu, í flipanum **Bylgja**, í flokknum **Tengdar upplýsingar**, skal velja **Vinna** til að skoða vinnuna sem var búin til.</span><span class="sxs-lookup"><span data-stu-id="4486d-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="4486d-427">Skráið niður vinnukennið.</span><span class="sxs-lookup"><span data-stu-id="4486d-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="4486d-428">Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Úthlutanir á röðunarstað á útleið**.</span><span class="sxs-lookup"><span data-stu-id="4486d-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="4486d-429">Í vinstri dálknum er hægt að skoða röðunarstaði á útleið sem voru búnir til fyrir hverja sendingu.</span><span class="sxs-lookup"><span data-stu-id="4486d-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="4486d-430">Í flýtiflipanum **Skilyrði staðsetningarflokkunar** er hægt að skoða auðkenni sendingarinnar fyrir þessa stöðu.</span><span class="sxs-lookup"><span data-stu-id="4486d-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="4486d-431">Eitt vinnukenni hefur verið búið til að færa birgðir úr tiltektarstaðsetningu í röðunarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4486d-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="4486d-432">Til að ljúka vinnunni þarftu vinnukennið sem var búið til í bylgjuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="4486d-433">Tínsla sölupöntunar yfir í röðunarstaðsetningu</span><span class="sxs-lookup"><span data-stu-id="4486d-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="4486d-434">Skráðu þig inn í forrit fartækisins sem starfsmaður í vöruhúsi *62*.</span><span class="sxs-lookup"><span data-stu-id="4486d-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="4486d-435">Í aðalvalmyndinni skal velja **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="4486d-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="4486d-436">Í valmyndinni **Á útleið** skal velja **Sölutiltekt**.</span><span class="sxs-lookup"><span data-stu-id="4486d-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="4486d-437">Veljið reitinn **Auðkenni** og færið síðan inn vinnukennið úr bylgjuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="4486d-438">Staðfestu færsluna.</span><span class="sxs-lookup"><span data-stu-id="4486d-438">Confirm your entry.</span></span>

    <span data-ttu-id="4486d-439">Næst er beðið um að færa inn marknúmeraplötu (NP).</span><span class="sxs-lookup"><span data-stu-id="4486d-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="4486d-440">Takið eftir því að lína 1 í sölupöntun 1 er það sem verður að tína og bæta við marknúmeraplötuna.</span><span class="sxs-lookup"><span data-stu-id="4486d-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="4486d-441">Vörunúmerið, magnið, vörulýsingin og tiltektarstaðsetningin eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="4486d-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="4486d-442">Í reitinn **Marknúmeraplata** skal færa inn númer númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="4486d-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="4486d-443">Velja skal allar línur sem búnar voru til í bylgjunni sem unnið var úr og yfir í sömu marknúmeraplötuna.</span><span class="sxs-lookup"><span data-stu-id="4486d-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="4486d-444">Staðfestu færsluna.</span><span class="sxs-lookup"><span data-stu-id="4486d-444">Confirm your entry.</span></span>

    <span data-ttu-id="4486d-445">Fartækjaforritið birtir nú nokkrar síður af **Tiltekt** sem benda á tiltektarstaðsetninguna og vöruna og magnið sem þarf að tína.</span><span class="sxs-lookup"><span data-stu-id="4486d-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="4486d-446">Þegar búið er að bæta valinni vöru við númeraplötuna skal staðfesta tiltektina.</span><span class="sxs-lookup"><span data-stu-id="4486d-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="4486d-447">Síðasta síðan verður vinnan við að setja tíndar vörur í röðunarstaðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="4486d-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="4486d-448">Staðfestið fyrstu tiltektina.</span><span class="sxs-lookup"><span data-stu-id="4486d-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="4486d-449">Næsta tiltekt er sýnd.</span><span class="sxs-lookup"><span data-stu-id="4486d-449">The next pick work is shown.</span></span> <span data-ttu-id="4486d-450">Staðfesta tínslu.</span><span class="sxs-lookup"><span data-stu-id="4486d-450">Confirm the pick.</span></span>
1. <span data-ttu-id="4486d-451">Haldið áfram að staðfesta eftirstandandi tiltektir.</span><span class="sxs-lookup"><span data-stu-id="4486d-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="4486d-452">Síðasta skrefið er að ljúka frágangsvinnunni.</span><span class="sxs-lookup"><span data-stu-id="4486d-452">The last step is to complete the put work.</span></span> <span data-ttu-id="4486d-453">Staðfestið frágang yfir á röðunarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4486d-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="4486d-454">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="4486d-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="4486d-455">Lokið **Tiltekt sölu** í forriti fartækis.</span><span class="sxs-lookup"><span data-stu-id="4486d-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="4486d-456">Röðun/setja á vegg</span><span class="sxs-lookup"><span data-stu-id="4486d-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="4486d-457">Nú þegar búið er að koma öllum birgðum fyrir í röðunarstaðsetningunni, þarf að raða þeim á rétta röðunarstaði.</span><span class="sxs-lookup"><span data-stu-id="4486d-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="4486d-458">Skráið ykkur inn í forrit fartækis.</span><span class="sxs-lookup"><span data-stu-id="4486d-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="4486d-459">Í aðalvalmyndinni skal velja **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="4486d-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="4486d-460">Í valmyndinni **Útleið** skal velja **Raða** til að hefja röðun á vörum.</span><span class="sxs-lookup"><span data-stu-id="4486d-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="4486d-461">Í reitinn **NP/GÁM** skal færa inn marknúmeraplötu fyrir sölupöntunarvinnuna sem var tínd.</span><span class="sxs-lookup"><span data-stu-id="4486d-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="4486d-462">Staðfestu færsluna.</span><span class="sxs-lookup"><span data-stu-id="4486d-462">Confirm your entry.</span></span>
1. <span data-ttu-id="4486d-463">Sláið inn vörunúmerið sem á fyrst að raða.</span><span class="sxs-lookup"><span data-stu-id="4486d-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="4486d-464">Kerfið ákvarðar fyrsta röðunarstaðinn sem á að sýna.</span><span class="sxs-lookup"><span data-stu-id="4486d-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="4486d-465">Staðfestið röðunarstaðinn.</span><span class="sxs-lookup"><span data-stu-id="4486d-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="4486d-466">Beðið er um að númeraplötu verði úthlutað á röðunarstaðinn.</span><span class="sxs-lookup"><span data-stu-id="4486d-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="4486d-467">Veljið reitinn **NP**, færið inn númer númeraplötu og staðfestið síðan innsláttinn.</span><span class="sxs-lookup"><span data-stu-id="4486d-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="4486d-468">Röðunarstaðurinn tengist auðkenni sendingar og því þarf að raða tíndum vörum á númeraplötu sem á við þessa tilteknu sendingu á útleið og sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="4486d-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="4486d-469">Næsta síðan sýnir vörukennið, magn, staðsetningarkenni röðunar og auðkenni „frá“ (tiltekt) og „til“ (röðun) númeraplatnanna.</span><span class="sxs-lookup"><span data-stu-id="4486d-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="4486d-470">Upplýsingarnar á þessari síðu segja þér að raða tiltekinni vöru og magni frá númeraplötu tiltektar í númeraplötu röðunar.</span><span class="sxs-lookup"><span data-stu-id="4486d-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="4486d-471">Staðfestið röðunarstaðinn.</span><span class="sxs-lookup"><span data-stu-id="4486d-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="4486d-472">Raðið vörunum í fyrstu röðunarstaðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="4486d-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="4486d-473">Þegar þessu er lokið beinir kerfið þér að næsta röðunarstað.</span><span class="sxs-lookup"><span data-stu-id="4486d-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="4486d-474">Endurtakið þetta ferli fyrir allar tíndar línur í vinnubeiðninni.</span><span class="sxs-lookup"><span data-stu-id="4486d-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="4486d-475">Einnig ætti að nota þetta ferli þegar margar tiltektarlínur eru með sama vörunúmerið.</span><span class="sxs-lookup"><span data-stu-id="4486d-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="4486d-476">Þegar þetta ferli er endurtekið fyrir allar vörurnar, metur kerfið skilyrðið úr næstu skönnuðu vöru (vinnulínu) og ákveður hvaða röðunarstaðsetningu ætti að setja hana í.</span><span class="sxs-lookup"><span data-stu-id="4486d-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="4486d-477">Þér er sjálfkrafa sagt að setja vöruna á rétta röðunarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4486d-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="4486d-478">Það fer eftir uppsetningu staðfestingar, en þér er einnig sagt að staðfesta þessa aðgerð með því að slá inn númer staðsetningar eða auðkenni númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="4486d-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4486d-479">Ef kveikt er á sjálfvirkri röðun, er handvirk hnekking ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="4486d-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="4486d-480">Þegar þessu er lokið, í Microsoft Dynamics 365 Supply Chain Management, skal opna síðuna **Úthlutanir á röðunarstaðsetningum á útleið** til að fara yfir stöðuna á staðsetningunum.</span><span class="sxs-lookup"><span data-stu-id="4486d-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="4486d-481">Ef staðsetningum er lokað sjálfkrafa skal velja **Sýna lokaðar** til að sýna lokaðar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="4486d-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="4486d-482">Takið eftir að færslur röðunarstaðsetningar eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="4486d-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="4486d-483">Varan og magnið sem unnið var úr í gegnum staðsetninguna er sýnt.</span><span class="sxs-lookup"><span data-stu-id="4486d-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="4486d-484">Þegar flokkunarsniðmát á útleið er sett upp, er valkosturinn **Loka sjálfkrafa röðun staðsetningar** stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="4486d-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="4486d-485">Þess vegna er staðsetningunni lokað sjálfkrafa þegar síðustu væntanlegu birgðirnar eru settar í hana.</span><span class="sxs-lookup"><span data-stu-id="4486d-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="4486d-486">Röðunarstaðsetningarnar eru í stöðunni **Lokað** og vinna hefur verið búin til að flytja raðaðar birgðir yfir á staðsetninguna *Útskot*.</span><span class="sxs-lookup"><span data-stu-id="4486d-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="4486d-487">Ljúkið tiltekt á röðuðum birgðum til að færa birgðirnar yfir á sendingarstaðinn.</span><span class="sxs-lookup"><span data-stu-id="4486d-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="4486d-488">Þegar birgðir eru tilbúnar skal staðfesta sendingu.</span><span class="sxs-lookup"><span data-stu-id="4486d-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="4486d-489">Til að unnið verði rétt úr tiltekt raðaðra birgða, ætti valmyndaratriði fartækis, sem er með vinnuklasakenni þar sem reiturinn **Gerð vinnubeiðni** er stilltur á *Tiltekt raðaðra birgða*, að vera notað fyrir flutnings- og hleðsluferlið.</span><span class="sxs-lookup"><span data-stu-id="4486d-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="4486d-490">Loka staðsetningu handvirkt (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="4486d-490">Manually close a position (optional)</span></span>

<span data-ttu-id="4486d-491">Ef loka á röðunarstaðsetningum handvirkt, verður valkosturinn **Loka sjálfkrafa röðun staðsetningar** fyrir flokkunarsniðmát á útleið að vera stillt á *Nei* og lokun verður að gera áður en hægt er að færa birgðir yfir á útskotssvæðið.</span><span class="sxs-lookup"><span data-stu-id="4486d-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="4486d-492">Hægt er að loka stöðum á ýmsa vegu:</span><span class="sxs-lookup"><span data-stu-id="4486d-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="4486d-493">Um vöruhúsaforrit:</span><span class="sxs-lookup"><span data-stu-id="4486d-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="4486d-494">Notandinn getur skannað eina vöruna sem er þegar í staðsetningunni og síðan valið **Loka** til að loka henni.</span><span class="sxs-lookup"><span data-stu-id="4486d-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="4486d-495">Ef notandi skannar gám sem þegar hefur verið raðað á gám, birtast villuboð.</span><span class="sxs-lookup"><span data-stu-id="4486d-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="4486d-496">Notandinn getur samt haldið áfram að loka staðnum.</span><span class="sxs-lookup"><span data-stu-id="4486d-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="4486d-497">Af Microsoft Dynamics 365 Supply Chain Management síðunni **Úthlutanir á röðunarstaðsetningu á útleið**:</span><span class="sxs-lookup"><span data-stu-id="4486d-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="4486d-498">Notandinn getur valið færslu röðunarstaðsetningu á útleið og síðan valið **Loka staðsetningu** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="4486d-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="4486d-499">Ábendingar</span><span class="sxs-lookup"><span data-stu-id="4486d-499">Tips</span></span>

- <span data-ttu-id="4486d-500">Ekki er hægt að færa vörur milli staða þegar búið er að úthluta þeim einni slíkri.</span><span class="sxs-lookup"><span data-stu-id="4486d-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="4486d-501">Kerfið metur hversu mikið af hverri vöru ætti að fara á tiltekin stað.</span><span class="sxs-lookup"><span data-stu-id="4486d-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="4486d-502">Flokkunarsniðmát er hægt að skilgreina til að búa sjálfkrafa til gáma þegar staðir eru lokaðir.</span><span class="sxs-lookup"><span data-stu-id="4486d-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="4486d-503">Þessi nálgun býr til hefðbundið skipulag gámakennis sem byggir á tiltekinni pökkunarforstillingu.</span><span class="sxs-lookup"><span data-stu-id="4486d-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4486d-504">Þegar vinna birgðahreyfingar hefur verið búin til í röðunarstaðsetningu, má ekki hætta við vinnuna.</span><span class="sxs-lookup"><span data-stu-id="4486d-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="4486d-505">Annars verður staðnum og gámum hans eytt úr kerfinu og ekki tiltækir fyrir frekari úrvinnslu.</span><span class="sxs-lookup"><span data-stu-id="4486d-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="4486d-506">Birgðir verða einnig fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="4486d-506">The inventory will also be removed.</span></span>
