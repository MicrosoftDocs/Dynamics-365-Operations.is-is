---
title: Setja upp og nota prentun bylgjumerkja
description: Þetta efnisatriði lýsir prentun bylgjumerkja og útskýrir hvernig á að setja hana upp.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: a08f10c1f5c3ff5b9023f37614c4e113b3a6b30d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211767"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="85f50-103">Setja upp og nota prentun bylgjumerkja</span><span class="sxs-lookup"><span data-stu-id="85f50-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85f50-104">Prentun bylgjumerkja býður upp á aðra leið til að prenta merki með því að kynna nýja aðferð bylgjuskrefs sem gerir þér kleift að búa til og prenta merki beint úr bylgjusniðmátinu meðan á bylgjuframkvæmd stendur.</span><span class="sxs-lookup"><span data-stu-id="85f50-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="85f50-105">Þess vegna verða merkin þegar tiltæk áður en starfsmenn keyra verkbeiðnina í fartæki.</span><span class="sxs-lookup"><span data-stu-id="85f50-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="85f50-106">Starfsmenn geta síðan hengt nauðsynleg merki við meðan tiltekt er í gangi í staðinn fyrir að gera það eftir á.</span><span class="sxs-lookup"><span data-stu-id="85f50-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="85f50-107">Prentun bylgjumerkis notar Zebra forritunarmál til að búa til útlit merkja.</span><span class="sxs-lookup"><span data-stu-id="85f50-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="85f50-108">Útlit merkis skiptist í þrjá hluta (síðuhaus, meginmál og síðufót) til að bjóða upp á merki sem eru með endurtekið skipulag.</span><span class="sxs-lookup"><span data-stu-id="85f50-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="85f50-109">Sniðmát bylgjumerkja segja kerfinu hvaða útlit merkis á að nota.</span><span class="sxs-lookup"><span data-stu-id="85f50-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="85f50-110">Notendur geta tilgreint hvaða prentari er notaður.</span><span class="sxs-lookup"><span data-stu-id="85f50-110">Users can specify which printer is used.</span></span> <span data-ttu-id="85f50-111">Þeir geta einnig prentað merki á nokkrum prenturum á sama tíma eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="85f50-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="85f50-112">Síðan **Ferill bylgjumerkis** sýnir skrá yfir öll merki sem hafa verið búin til með því að nota þessa uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="85f50-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="85f50-113">Þú getur flokkað saman merki út frá vinnuhausum, þú getur prentað sundurliðunarmerki fyrir hvern vinnuhaus og þú getur prentað merki fyrir gámainnihald, merkimiða á pakkningar og svipuð merki.</span><span class="sxs-lookup"><span data-stu-id="85f50-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="85f50-114">Þessi virkni kemur ekki í stað núverandi prentunarvirkni merkimiða sem byggir á skjalaleið.</span><span class="sxs-lookup"><span data-stu-id="85f50-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="85f50-115">Prentun bylgjumerkis býður upp á eftirfarandi viðbætur:</span><span class="sxs-lookup"><span data-stu-id="85f50-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="85f50-116">Prentaðu merkimiða í samræmi við kassafjölda í einni vinnulínu, án þess að nota gámun.</span><span class="sxs-lookup"><span data-stu-id="85f50-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="85f50-117">(„Kassi“ er eining sem er úthlutað á röðunarflokkslínu einingar.)</span><span class="sxs-lookup"><span data-stu-id="85f50-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="85f50-118">Prentaðu nokkrar mismunandi merkjaraðir (til dæmis merki fyrir kassa og bretti).</span><span class="sxs-lookup"><span data-stu-id="85f50-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="85f50-119">Hafðu með tölusetningu merkis (til dæmis 1/124, 2/124, ... 124/124) og skilgreindu svið tölusetningar (til dæmis vinnulínu, hleðslínu eða sendingu).</span><span class="sxs-lookup"><span data-stu-id="85f50-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="85f50-120">Stofnaðu og prentaðu auðkenni farmbréfs á merki áður en farmbréfið er búið til.</span><span class="sxs-lookup"><span data-stu-id="85f50-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="85f50-121">Búðu til einkvæmt raðnúmer vörusendingar (SSCC) fyrir hvern kassa og láttu það fylgja með hverjum merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="85f50-122">Búðu til númeraröð sem fylgir GS1 fyrir auðkenni farmbréfa og raðnúmera vörusendinga.</span><span class="sxs-lookup"><span data-stu-id="85f50-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="85f50-123">Prentaðu aftur merkimiða úr bæði fartækjum og fjölhæfum biðlara.</span><span class="sxs-lookup"><span data-stu-id="85f50-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="85f50-124">Ógiltu merki (til dæmis í stuttum tiltektum) og prentaðu þau aftur.</span><span class="sxs-lookup"><span data-stu-id="85f50-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="85f50-125">Hreinsa feril bylgjumerkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="85f50-126">Endurbætur á skipulagi skjalaleiða er deilt á milli skipulags skjalaleiðar og útlits bylgjumerkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="85f50-127">(Frekari upplýsingar er að finna í [Skipulag skjalaleiðar fyrir númeraplötur](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="85f50-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="85f50-128">Þessar endurbætur gera það skilvirkara að merkja kassa fyrir röðun á bretti.</span><span class="sxs-lookup"><span data-stu-id="85f50-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="85f50-129">Þær gagnast sérstaklega fyrirtækjum sem senda til stórra smásala sem staðfesta sjálfkrafa innhreyfingar pantana með því að skanna hvern kassa fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="85f50-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="85f50-130">Þú getur innleitt stillingar atburðarásina sem lýst er í þessu efnisatriði annaðhvort hvort fyrir sig eða í samsetningu, fer allt eftir kröfum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="85f50-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="85f50-131">Þú getur hannað nokkur sniðmát bylgjumerkis sem virka í röð (eins og sýnt er í atburðarás 3).</span><span class="sxs-lookup"><span data-stu-id="85f50-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="85f50-132">Til dæmis er hægt að nota atburðarás 1 til að prenta kassamiða og atburðarás 2 til að prenta brettamiða (ef bretti á lager eru mismunandi að stærð og samsetningu).</span><span class="sxs-lookup"><span data-stu-id="85f50-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="85f50-133">Kveikja á prentunareiginleika bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="85f50-134">Áður en hægt er að nota eiginleikann *Prentun bylgjumerkis* verður að vera kveikt á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="85f50-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="85f50-135">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="85f50-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="85f50-136">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="85f50-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="85f50-137">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="85f50-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="85f50-138">**Heiti eiginleika:** *Prentun bylgjumerkis*</span><span class="sxs-lookup"><span data-stu-id="85f50-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="85f50-139">Atburðarás 1: Prentun bylgjumerkis þar sem eitt bylgjumerki er búið til</span><span class="sxs-lookup"><span data-stu-id="85f50-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="85f50-140">Þessi atburðarás sýnir hvernig fyrirtæki getur prentað merkimiða fyrir stóran smásöluaðila sem staðfestir sjálfkrafa innhreyfingar pöntunar með því að skanna hvern kassa fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="85f50-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="85f50-141">Þessi atburðarás sýnir verkflæðið frá upphafi til enda.</span><span class="sxs-lookup"><span data-stu-id="85f50-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="85f50-142">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="85f50-142">Make demo data available</span></span>

<span data-ttu-id="85f50-143">Til að fylgja þessari atburðarás verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann **USMF**.</span><span class="sxs-lookup"><span data-stu-id="85f50-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="85f50-144">Ganga skal úr skugga um að aðferð bylgjumerkis sé tiltæk</span><span class="sxs-lookup"><span data-stu-id="85f50-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="85f50-145">Þú gætir þurft að endurgera aðferðir bylgjuferlisins til að gera prentunaraðferð bylgjumerkis tiltæka.</span><span class="sxs-lookup"><span data-stu-id="85f50-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="85f50-146">Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.</span><span class="sxs-lookup"><span data-stu-id="85f50-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="85f50-147">Staðfestu að **waveLabelPrinting** sé á listanum.</span><span class="sxs-lookup"><span data-stu-id="85f50-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="85f50-148">Ef svo er ekki skal velja **Endurgera aðferðir** á aðgerðasvæðinu til að bæta því við.</span><span class="sxs-lookup"><span data-stu-id="85f50-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="85f50-149">Skilgreina bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="85f50-149">Configure a wave template</span></span>

<span data-ttu-id="85f50-150">Bylgjusniðmát leyfa þér að tengja sérstök tilvik af bylgjuaðferðum við samsvarandi sniðmát bylgjumerkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="85f50-151">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="85f50-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="85f50-152">Veldu sniðmát, t.d. **62 Sjálfgefin sending**.</span><span class="sxs-lookup"><span data-stu-id="85f50-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="85f50-153">Í flýtiflipanum **Aðferðir** skal færa aðferðina **Prentun bylgjumerkis** í dálkinn **Valdar aðferðir**.</span><span class="sxs-lookup"><span data-stu-id="85f50-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="85f50-154">Í dálknum **Valdar aðferðir** skal velja aðferðina **Prentun bylgjumerkis** og stilla reitinn **Kóði bylgjuskrefs** á *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="85f50-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="85f50-155">Frekari upplýsingar um bylgjuskrefakóða er að finna í [Kóðar bylgjuskrefs](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="85f50-156">Búa til útlit bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-156">Create a wave label layout</span></span>

<span data-ttu-id="85f50-157">Útlit merkimiðans stýrir því hvaða upplýsingar eru prentaðar á merkimiðann og hvernig þær eru settar fram. Hér færir þú inn ZPL-kóðann sem er sendur á prentarann.</span><span class="sxs-lookup"><span data-stu-id="85f50-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="85f50-158">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Útlit bylgjumerkja**.</span><span class="sxs-lookup"><span data-stu-id="85f50-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="85f50-159">Búið til færslu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="85f50-160">**Útlitskenni merkis:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="85f50-161">**Lýsing:** *Pakki (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="85f50-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="85f50-162">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-163">Á aðgerðasvæðinu skal velja **Línustillingar bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="85f50-164">Síðan **Línustillingar bylgjumerkis** birtist.</span><span class="sxs-lookup"><span data-stu-id="85f50-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="85f50-165">Hér er hægt að skilgreina breytilega hluta merkingarinnar.</span><span class="sxs-lookup"><span data-stu-id="85f50-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="85f50-166">Bætið við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-167">**Línukenni:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="85f50-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="85f50-168">**Töfluheiti línu:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="85f50-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="85f50-169">**Upphafsstaða línu:** *0*</span><span class="sxs-lookup"><span data-stu-id="85f50-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="85f50-170">Þessi reitur skilgreinir lóðréttu stöðuna þar sem línan byrjar á merkimiðanum.</span><span class="sxs-lookup"><span data-stu-id="85f50-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="85f50-171">**Línuhæð:** *0*</span><span class="sxs-lookup"><span data-stu-id="85f50-171">**Row height:** *0*</span></span>

        <span data-ttu-id="85f50-172">Þessi reitur skilgreinir hæð hverrar línu (í punktum), í samræmi við ZPL-staðalinn.</span><span class="sxs-lookup"><span data-stu-id="85f50-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="85f50-173">Hæð línunnar er jákvæð fyrir lárétta merkimiða og neikvæð fyrir lóðrétta merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="85f50-174">Fyrst að það er aðeins ein lína í þessu dæmi, er hægt að stilla gildið á *0* (núll).</span><span class="sxs-lookup"><span data-stu-id="85f50-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="85f50-175">**Línur á síðu:** *1*</span><span class="sxs-lookup"><span data-stu-id="85f50-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="85f50-176">Þessi reitur skilgreinir fjölda lína sem hægt er að prenta á hvern merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="85f50-177">Þessi uppsetning leiðir til þess að aðskilinn ZPL-merkimiði er prentaður fyrir hverja færslu í töflu bylgjumerkja.</span><span class="sxs-lookup"><span data-stu-id="85f50-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="85f50-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="85f50-178">Close the page.</span></span>
1. <span data-ttu-id="85f50-179">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="85f50-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="85f50-180">Í svarglugga fyrirspurnarritils á flipanum **Svið** skal bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="85f50-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-181">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-182">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-183">**Svæði:** *Gerð vinnu*</span><span class="sxs-lookup"><span data-stu-id="85f50-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="85f50-184">**Skilyrði:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="85f50-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="85f50-185">Þessi fyrirspurn tryggir að aðeins vinnulínur af tiltektargerð verði prentaðar á merkimiðann, ekki vinnulínur frágangs.</span><span class="sxs-lookup"><span data-stu-id="85f50-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="85f50-186">Ef ætlunin er að geta prentað auðkenni farmbréfsins, skal í flipanum **Samtengingar** velja töfluna **Vinnulínur** og tengja töfluna **Sendingar** við það.</span><span class="sxs-lookup"><span data-stu-id="85f50-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="85f50-187">Lokið svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="85f50-188">Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**.</span><span class="sxs-lookup"><span data-stu-id="85f50-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="85f50-189">Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn kóða fyrir nauðsynlegan síðuhaus.</span><span class="sxs-lookup"><span data-stu-id="85f50-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="85f50-190">Ef til dæmis Zebra-prentari er notaður er hægt að nota eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="85f50-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="85f50-191">Í hlutanum **Hluti meginmáls**, í reitinn **Meginmál merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegt meginmál.</span><span class="sxs-lookup"><span data-stu-id="85f50-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="85f50-192">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="85f50-193">Í hlutanum **Hluti síðufóts**, í reitinn **Síðufótur merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðufót.</span><span class="sxs-lookup"><span data-stu-id="85f50-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="85f50-194">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="85f50-195">Þessi uppsetning prentar eitt eintak af hverjum merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="85f50-196">Ef þörf er á fleiri eintökum (til dæmis eitt eintak fyrir hverja hlið brettisins) skal stilla gildið **n** fyrir hlutann **\^PQn** í síðufætinum á þann fjölda eintaka sem þarf.</span><span class="sxs-lookup"><span data-stu-id="85f50-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="85f50-197">Til dæmis, til að prenta fjögur eintök af hverjum merkimiða skal gefa upp **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="85f50-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="85f50-198">Nú er merkimiðinn tilbúinn til notkunar.</span><span class="sxs-lookup"><span data-stu-id="85f50-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="85f50-199">Stofna bylgjusniðmátsgerð</span><span class="sxs-lookup"><span data-stu-id="85f50-199">Create a wave label type</span></span>

<span data-ttu-id="85f50-200">Gerðir bylgjumerkis eru notaðar til að tengja sniðmát bylgjumerkis við einingu í línur röðunarflokkseininga.</span><span class="sxs-lookup"><span data-stu-id="85f50-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="85f50-201">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Gerðir bylgjumerkja**.</span><span class="sxs-lookup"><span data-stu-id="85f50-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="85f50-202">Bætið við gerð bylgjumerkis sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="85f50-203">**Merkimiðagerð:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="85f50-204">**Lýsing:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="85f50-205">Setja upp röðunarflokka eininga</span><span class="sxs-lookup"><span data-stu-id="85f50-205">Set up unit sequence groups</span></span>

<span data-ttu-id="85f50-206">Næst skal setja upp röðunarflokk einingar fyrir gerð bylgjumerkisins.</span><span class="sxs-lookup"><span data-stu-id="85f50-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="85f50-207">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Röðunarflokkar einingar**.</span><span class="sxs-lookup"><span data-stu-id="85f50-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="85f50-208">Veljið flokkinn **Ea Box PL**.</span><span class="sxs-lookup"><span data-stu-id="85f50-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="85f50-209">Fyrir línuna **Kassi** skal stilla reitinn **Gerð bylgjustigs** á *Kassi*.</span><span class="sxs-lookup"><span data-stu-id="85f50-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="85f50-210">Stofna sniðmát bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-210">Create a wave label template</span></span>

<span data-ttu-id="85f50-211">Næst skal stofna sniðmát bylgjumerkis fyrir gerð bylgjumerkisins.</span><span class="sxs-lookup"><span data-stu-id="85f50-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="85f50-212">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Sniðmát bylgjumerkja**.</span><span class="sxs-lookup"><span data-stu-id="85f50-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="85f50-213">Bætið við bylgjustigssniðmáti og stillið eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="85f50-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="85f50-214">**Heiti sniðmátsmerkis:** *Merkimiðar kassa*</span><span class="sxs-lookup"><span data-stu-id="85f50-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="85f50-215">**Lýsing:** *Merkimiðar kassa*</span><span class="sxs-lookup"><span data-stu-id="85f50-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="85f50-216">**Kóði bylgjuskrefs:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="85f50-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="85f50-217">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="85f50-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="85f50-218">Í flýtiflipanum **Almennt** skal stilla reitinn **Gerð bylgjumerkis** á *Kassi*.</span><span class="sxs-lookup"><span data-stu-id="85f50-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="85f50-219">Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal bæta við nýrri línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-220">**Útlitskenni merkis:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="85f50-221">**Heiti prentara:** Veljið viðeigandi ZPL-prentara.</span><span class="sxs-lookup"><span data-stu-id="85f50-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="85f50-222">**Keyra fyrirspurn:** *Já* (Þessi stilling er valfrjáls, en mælt er með henni til að hámarka afköst.)</span><span class="sxs-lookup"><span data-stu-id="85f50-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="85f50-223">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-224">Valfrjálst: Ef verið er að setja upp merkimiða sem hannaður er með ákveðinn viðskiptavin í huga, þarf að búa til fyrirspurn til að finna lykil viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="85f50-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="85f50-225">Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="85f50-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="85f50-226">Því næst, í svarglugga fyrirspurnarritils í flipanum **Svið**, skal bæta við línu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-227">**Tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="85f50-228">**Afleidd tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="85f50-229">**Reitur:** *Reikningsnúmer*</span><span class="sxs-lookup"><span data-stu-id="85f50-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="85f50-230">**Skilyrði:** Sláið inn viðeigandi númer viðskiptavinalykils.</span><span class="sxs-lookup"><span data-stu-id="85f50-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="85f50-231">Þegar því er lokið skal velja **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="85f50-232">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils fyrir allt merkjasniðmát.</span><span class="sxs-lookup"><span data-stu-id="85f50-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="85f50-233">Í svarglugga fyrirspurnarritils, í flipanum **Röðun**, skal bæta við línu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-234">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-235">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-236">**Reitur:** *Tilvísunarkenni hleðslulínu (færslukenni)*</span><span class="sxs-lookup"><span data-stu-id="85f50-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="85f50-237">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="85f50-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="85f50-238">Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="85f50-239">Skilaboðagluggi biður um að endurstillingaraðgerð flokkunar verði staðfest.</span><span class="sxs-lookup"><span data-stu-id="85f50-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="85f50-240">Veldu **Já** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="85f50-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="85f50-241">Á aðgerðasvæðinu skal velja **Sniðmátsflokkur bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="85f50-242">Í svarglugganum **Sniðmátsflokkur bylgjumerkis** skal velja línuna þar sem reiturinn **Heiti tilvísunarreits** er stillt á *Tilvísunarkenni hleðslulínu* og síðan velja gátreitinn **Smíðakenni merkis** fyrir þessa línu.</span><span class="sxs-lookup"><span data-stu-id="85f50-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85f50-243">Þessi uppsetning býr til eina merkimiðaröð („Kassi 1 af X“) fyrir hverja hleðslulínu í gegnum bylgjuna, óháð uppsetningu vinnuflokkunar.</span><span class="sxs-lookup"><span data-stu-id="85f50-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="85f50-244">Hægt er að prenta þessa röðun merkimiða á útlit merkimiðans.</span><span class="sxs-lookup"><span data-stu-id="85f50-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="85f50-245">Skilgreina viðbætur númeraraðar</span><span class="sxs-lookup"><span data-stu-id="85f50-245">Configure number sequence extensions</span></span>

<span data-ttu-id="85f50-246">Viðbætur númeraraðar stjórna GS1-reglufylgni tiltekinna númeraraða.</span><span class="sxs-lookup"><span data-stu-id="85f50-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="85f50-247">Þessi skilgreining er valfrjáls fyrir núverandi atburðarás.</span><span class="sxs-lookup"><span data-stu-id="85f50-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="85f50-248">Nánari upplýsingar og leiðbeiningar um skilgreiningar er að finna í [Skilgreina viðbætur númeraraðar](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="85f50-249">Stofna sölupöntun og losa hana í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="85f50-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="85f50-250">Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="85f50-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="85f50-251">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="85f50-252">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="85f50-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="85f50-253">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="85f50-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="85f50-254">Bætið við tveimur sölupöntunarlínum sem eru með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="85f50-255">Sölupöntun lína 1:</span><span class="sxs-lookup"><span data-stu-id="85f50-255">Sales order line 1:</span></span>

        - <span data-ttu-id="85f50-256">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="85f50-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="85f50-257">**Magn:** *9024*</span><span class="sxs-lookup"><span data-stu-id="85f50-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="85f50-258">**Eining:** *ea* (9024 ea = 376 Kassi = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="85f50-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="85f50-259">Sölupöntun lína 2:</span><span class="sxs-lookup"><span data-stu-id="85f50-259">Sales order line 2:</span></span>

        - <span data-ttu-id="85f50-260">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="85f50-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="85f50-261">**Magn:** *9016*</span><span class="sxs-lookup"><span data-stu-id="85f50-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="85f50-262">**Eining:** *ea* (9016 ea = 322 Kassi = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="85f50-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="85f50-263">Vörurnar og magnið sem er gefið upp hér er aðeins notað sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="85f50-264">Nota verður röðunarflokk einingar sem var skilgreindur áður, viðeigandi umreikninga eininga úr *ea* í *Kassi* í *PL* verður að vera skilgreint fyrir þær og þær að vera með birgðastöðu í vöruhúsi *62*.</span><span class="sxs-lookup"><span data-stu-id="85f50-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="85f50-265">Frekari upplýsingar er að finna í [Mælieining og birgðareglur](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="85f50-266">Velja sölupöntunarlínu 1.</span><span class="sxs-lookup"><span data-stu-id="85f50-266">Select sales order line 1.</span></span> <span data-ttu-id="85f50-267">Því næst skal, í hlutanum **Sölupöntunarlína**, í valmyndinni **Birgðir**, velja **Frátekningar**.</span><span class="sxs-lookup"><span data-stu-id="85f50-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="85f50-268">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** og loka svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="85f50-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="85f50-269">Endurtakið skref 4 og 5 fyrir sölupöntunarlínu 2.</span><span class="sxs-lookup"><span data-stu-id="85f50-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="85f50-270">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="85f50-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="85f50-271">Eftirfarandi tilvik gerast:</span><span class="sxs-lookup"><span data-stu-id="85f50-271">The following events occur:</span></span>

    - <span data-ttu-id="85f50-272">Kerfið vinnur úr stofnaðri sendingu með því að nota sniðmátið sem felur í sér prentunarstig merkisins.</span><span class="sxs-lookup"><span data-stu-id="85f50-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="85f50-273">Útlit merkisins verður notað til að skilgreina snið merkisins og niðurstaðan verður merki sem prentað er á prentara sem valinn er í sniðmáti merkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="85f50-274">Bylgjumerki eru búin til og prentuð.</span><span class="sxs-lookup"><span data-stu-id="85f50-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="85f50-275">Fjöldi merkimiða verður sá sami og kassafjöldinn (í þessu dæmi, 376 kassamerki fyrir línu 1 og 322 kassamerki fyrir línu 2).</span><span class="sxs-lookup"><span data-stu-id="85f50-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="85f50-276">Nýtt auðkenni farmbréfs er búið til fyrir sendingarnar.</span><span class="sxs-lookup"><span data-stu-id="85f50-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="85f50-277">Ef þú skilgreindir viðbætur númeraraðarinnar mun auðkenni bylgjumerkis fylgja **SSCC-18** númerasniðinu.</span><span class="sxs-lookup"><span data-stu-id="85f50-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="85f50-278">Hægt er að skoða og endurprenta bylgjumerki á eftirfarandi síðum.</span><span class="sxs-lookup"><span data-stu-id="85f50-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="85f50-279">Á aðgerðasvæði hverrar síðu, í flipanum **Sendingar**, í flokknum **Tengdar upplýsingar**, skal velja **Bylgjumerki**.</span><span class="sxs-lookup"><span data-stu-id="85f50-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="85f50-280">Allar sendingar \> Upplýsingar sendingar</span><span class="sxs-lookup"><span data-stu-id="85f50-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="85f50-281">Allar hleðslur \> Upplýsingar um hleðslu</span><span class="sxs-lookup"><span data-stu-id="85f50-281">All loads \> Load details</span></span>
- <span data-ttu-id="85f50-282">Allar bylgjur</span><span class="sxs-lookup"><span data-stu-id="85f50-282">All waves</span></span>
- <span data-ttu-id="85f50-283">Bylgjumerki</span><span class="sxs-lookup"><span data-stu-id="85f50-283">Wave labels</span></span>
- <span data-ttu-id="85f50-284">Ferill bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="85f50-285">Atburðarás 2: Prentun bylgjumerkis fyrir gámun (án færslna bylgjumerkis)</span><span class="sxs-lookup"><span data-stu-id="85f50-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="85f50-286">Þessi atburðarás gerir þér kleift að prenta bylgjumerki þegar þú notar gámun til að sjálfkrafa skipta upp vörum í kassa og þarf þar af leiðandi ekki færslu bylgjumerkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="85f50-287">Í þessu tilfelli virkar gámakennið sem staðgengill fyrir SSCC.</span><span class="sxs-lookup"><span data-stu-id="85f50-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="85f50-288">Hér er helsti munurinn á þessari atburðarás og atburðarás 1:</span><span class="sxs-lookup"><span data-stu-id="85f50-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="85f50-289">**Sniðmát bylgjumerkja:** Ekki er valin gerð bylgjumerkis í sniðmáti bylgjumerkis og ekki þarf flokkun merkjasmíðar.</span><span class="sxs-lookup"><span data-stu-id="85f50-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="85f50-290">Annars verður sniðmát bylgjumerkis skilgreint og tengt við bylgjusniðmátið á sama hátt og lýst er í atburðarás 1.</span><span class="sxs-lookup"><span data-stu-id="85f50-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="85f50-291">Skilja verður gerð bylgjumerkis eftir autt til að koma í veg fyrir bylgjumerki verði búin til.</span><span class="sxs-lookup"><span data-stu-id="85f50-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="85f50-292">**Útlit bylgjumerkja:** Þú munt skilgreina stillingar línuútlits bylgjumerkis fyrir vinnulínur í staðinn fyrir færslur bylgjumerkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="85f50-293">Skilgreina verður línustillinguna fyrir útlit merkis með því að nota töfluna **WHSWorkLine** í staðinn fyrir töfluna **WHSWaveLabel**.</span><span class="sxs-lookup"><span data-stu-id="85f50-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="85f50-294">Stillingin **Línur á síðu** stjórnar fjölda lína sem verða í meginmálinu.</span><span class="sxs-lookup"><span data-stu-id="85f50-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="85f50-295">Þessi skilgreining er einnig hentug fyrir atburðarásir fyrirtækis þar sem margvíslegar vörur eru pakkaðar í einn merktan kassa eða raðað á bretti og þetta pökkunarferli er hægt að skilgreina eftir vinnustofnun (t.d. vinna sem er flokkuð eftir sendingu).</span><span class="sxs-lookup"><span data-stu-id="85f50-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="85f50-296">Þessi atburðarás sýnir verkflæðið frá upphafi til enda.</span><span class="sxs-lookup"><span data-stu-id="85f50-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="85f50-297">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="85f50-297">Make demo data available</span></span>

<span data-ttu-id="85f50-298">Til að fylgja þessari atburðarás verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann **USMF**.</span><span class="sxs-lookup"><span data-stu-id="85f50-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="85f50-299">Ganga skal úr skugga um að aðferð bylgjumerkis sé tiltæk</span><span class="sxs-lookup"><span data-stu-id="85f50-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="85f50-300">Þú gætir þurft að endurgera aðferðir bylgjuferlisins til að gera prentunaraðferð bylgjumerkis tiltæka.</span><span class="sxs-lookup"><span data-stu-id="85f50-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="85f50-301">Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.</span><span class="sxs-lookup"><span data-stu-id="85f50-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="85f50-302">Staðfestu að **waveLabelPrinting** sé á listanum.</span><span class="sxs-lookup"><span data-stu-id="85f50-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="85f50-303">Ef svo er ekki skal velja **Endurgera aðferðir** á aðgerðasvæðinu til að bæta því við.</span><span class="sxs-lookup"><span data-stu-id="85f50-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="85f50-304">Velja bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="85f50-304">Set up a wave template</span></span>

<span data-ttu-id="85f50-305">Bylgjusniðmát leyfa þér að tengja sérstök tilvik af bylgjuaðferðum við samsvarandi sniðmát bylgjumerkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="85f50-306">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="85f50-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="85f50-307">Veljið sniðmát, t.d. **63 Gámun**.</span><span class="sxs-lookup"><span data-stu-id="85f50-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="85f50-308">Í flýtiflipanum **Aðferðir** skal færa aðferðina **Prentun bylgjumerkis** í dálkinn **Valdar aðferðir**.</span><span class="sxs-lookup"><span data-stu-id="85f50-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="85f50-309">Í dálknum **Valdar aðferðir** skal velja aðferðina **Prentun bylgjumerkis** og stilla reitinn **Kóði bylgjuskrefs** á *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="85f50-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="85f50-310">Frekari upplýsingar um bylgjuskrefakóða er að finna í [Kóðar bylgjuskrefs](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="85f50-311">Búa til útlit bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-311">Create a wave label layout</span></span>

1. <span data-ttu-id="85f50-312">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Útlit bylgjumerkja**.</span><span class="sxs-lookup"><span data-stu-id="85f50-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="85f50-313">Búið til færslu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="85f50-314">**Útlitskenni merkis:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="85f50-315">**Lýsing:** *Pakki (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="85f50-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="85f50-316">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-317">Á aðgerðasvæðinu skal velja **Línustillingar bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="85f50-318">Síðan **Línustillingar bylgjumerkis** birtist.</span><span class="sxs-lookup"><span data-stu-id="85f50-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="85f50-319">Hér er hægt að skilgreina breytilega hluta merkingarinnar.</span><span class="sxs-lookup"><span data-stu-id="85f50-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="85f50-320">Bætið við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-321">**Línukenni:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="85f50-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="85f50-322">**Töfluheiti línu:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="85f50-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="85f50-323">**Upphafsstaða línu:** *500*</span><span class="sxs-lookup"><span data-stu-id="85f50-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="85f50-324">Þessi reitur skilgreinir lóðréttu stöðuna þar sem línan byrjar á merkimiðanum.</span><span class="sxs-lookup"><span data-stu-id="85f50-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="85f50-325">**Línuhæð:** *-50*</span><span class="sxs-lookup"><span data-stu-id="85f50-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="85f50-326">Þessi reitur skilgreinir hæð hverrar raðar.</span><span class="sxs-lookup"><span data-stu-id="85f50-326">This field defines the height of each row.</span></span> <span data-ttu-id="85f50-327">Hæð línunnar er jákvæð fyrir lárétta merkimiða og neikvæð fyrir lóðrétta merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="85f50-328">**Línur á síðu:** *5*</span><span class="sxs-lookup"><span data-stu-id="85f50-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="85f50-329">Þessi reitur skilgreinir fjölda lína sem hægt er að prenta á hvern merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="85f50-330">Þessi uppsetning prentar nokkur ZPL-merki á hverja vinnu þar sem hver síða getur innihaldið allt að fimm vinnulínur.</span><span class="sxs-lookup"><span data-stu-id="85f50-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="85f50-331">Til dæmis, ef merkimiði er prentaður fyrir gám sem hefur 12 línur, verða þrír merkimiðar prentaðir.</span><span class="sxs-lookup"><span data-stu-id="85f50-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="85f50-332">Ef þú vilt prenta sérstaka merkimiða fyrir hverja tiltektarlínu skaltu stilla þetta gildi á *1*.</span><span class="sxs-lookup"><span data-stu-id="85f50-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="85f50-333">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="85f50-333">Close the page.</span></span>
1. <span data-ttu-id="85f50-334">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="85f50-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="85f50-335">Í svarglugga fyrirspurnarritils á flipanum **Svið** skal bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="85f50-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-336">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-337">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-338">**Svæði:** *Gerð vinnu*</span><span class="sxs-lookup"><span data-stu-id="85f50-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="85f50-339">**Skilyrði:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="85f50-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="85f50-340">Ef ætlunin er að geta prentað auðkenni farmbréfsins, skal í flipanum **Samtengingar** velja töfluna **Vinnulínur** og tengja töfluna **Sendingar** við það.</span><span class="sxs-lookup"><span data-stu-id="85f50-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="85f50-341">Lokið svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="85f50-342">Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**.</span><span class="sxs-lookup"><span data-stu-id="85f50-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="85f50-343">Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn kóða fyrir nauðsynlegan síðuhaus.</span><span class="sxs-lookup"><span data-stu-id="85f50-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="85f50-344">Ef til dæmis Zebra-prentari er notaður er hægt að nota eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="85f50-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="85f50-345">Í hlutanum **Hluti meginmáls**, í reitinn **Meginmál merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegt meginmál.</span><span class="sxs-lookup"><span data-stu-id="85f50-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="85f50-346">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="85f50-347">Í hlutanum **Hluti síðufóts**, í reitinn **Síðufótur merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðufót.</span><span class="sxs-lookup"><span data-stu-id="85f50-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="85f50-348">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="85f50-349">Þessi uppsetning prentar eitt eintak af hverjum merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="85f50-350">Ef þörf er á fleiri eintökum (til dæmis eitt eintak fyrir hverja hlið brettisins) skal stilla gildið **n** fyrir hlutann **\^PQn** í síðufætinum á þann fjölda eintaka sem þarf.</span><span class="sxs-lookup"><span data-stu-id="85f50-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="85f50-351">Til dæmis, til að prenta fjögur eintök af hverjum merkimiða skal gefa upp **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="85f50-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="85f50-352">Nú er merkimiðinn tilbúinn til notkunar.</span><span class="sxs-lookup"><span data-stu-id="85f50-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="85f50-353">Stofna sniðmát bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-353">Create a wave label template</span></span>

1. <span data-ttu-id="85f50-354">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Sniðmát bylgjumerkja**.</span><span class="sxs-lookup"><span data-stu-id="85f50-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="85f50-355">Bætið við bylgjustigssniðmáti og stillið eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="85f50-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="85f50-356">**Heiti á sniðmáti merkis:** *Merkimiðar gáms*</span><span class="sxs-lookup"><span data-stu-id="85f50-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="85f50-357">**Lýsing:** *Merkimiðar gáms*</span><span class="sxs-lookup"><span data-stu-id="85f50-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="85f50-358">**Kóði bylgjuskrefs:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="85f50-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="85f50-359">**Vöruhús:** *63*</span><span class="sxs-lookup"><span data-stu-id="85f50-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="85f50-360">Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal bæta við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-361">**Útlitskenni merkis:** *Gámur*</span><span class="sxs-lookup"><span data-stu-id="85f50-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="85f50-362">**Heiti prentara:** Veljið viðeigandi ZPL-prentara.</span><span class="sxs-lookup"><span data-stu-id="85f50-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="85f50-363">**Keyra fyrirspurn:** *Já* (Þessi stilling er valfrjáls, en mælt er með henni til að hámarka afköst.)</span><span class="sxs-lookup"><span data-stu-id="85f50-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="85f50-364">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-365">Valfrjálst: Ef verið er að setja upp merkimiða sem hannaður er með ákveðinn viðskiptavin í huga, þarf að búa til fyrirspurn til að finna lykil viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="85f50-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="85f50-366">Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="85f50-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="85f50-367">Því næst, í svarglugga fyrirspurnarritils í flipanum **Svið**, skal bæta við línu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-368">**Tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="85f50-369">**Afleidd tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="85f50-370">**Reitur:** *Reikningsnúmer*</span><span class="sxs-lookup"><span data-stu-id="85f50-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="85f50-371">**Skilyrði:** Sláið inn viðeigandi númer viðskiptavinalykils.</span><span class="sxs-lookup"><span data-stu-id="85f50-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="85f50-372">Þegar því er lokið skal velja **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="85f50-373">Skilgreina viðbætur númeraraðar</span><span class="sxs-lookup"><span data-stu-id="85f50-373">Configure number sequence extensions</span></span>

<span data-ttu-id="85f50-374">Viðbætur númeraraðar stjórna GS1-reglufylgni tiltekinna númeraraða.</span><span class="sxs-lookup"><span data-stu-id="85f50-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="85f50-375">Þessi skilgreining er valfrjáls fyrir núverandi atburðarás.</span><span class="sxs-lookup"><span data-stu-id="85f50-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="85f50-376">Nánari upplýsingar og leiðbeiningar um skilgreiningar er að finna í [Skilgreina viðbætur númeraraðar](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="85f50-377">Stofna sölupöntun og losa hana í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="85f50-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="85f50-378">Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="85f50-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="85f50-379">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="85f50-380">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="85f50-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="85f50-381">**Vöruhús:** *63*</span><span class="sxs-lookup"><span data-stu-id="85f50-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="85f50-382">Bæta við fimm sölupöntunarlínum::</span><span class="sxs-lookup"><span data-stu-id="85f50-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="85f50-383">Sölupöntun lína 1:</span><span class="sxs-lookup"><span data-stu-id="85f50-383">Sales order line 1:</span></span>

        - <span data-ttu-id="85f50-384">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="85f50-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="85f50-385">**Magn:** *10*</span><span class="sxs-lookup"><span data-stu-id="85f50-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="85f50-386">Sölupöntun lína 2:</span><span class="sxs-lookup"><span data-stu-id="85f50-386">Sales order line 2:</span></span>

        - <span data-ttu-id="85f50-387">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="85f50-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="85f50-388">**Magn:** *20*</span><span class="sxs-lookup"><span data-stu-id="85f50-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="85f50-389">Sölupöntun lína 3:</span><span class="sxs-lookup"><span data-stu-id="85f50-389">Sales order line 3:</span></span>

        - <span data-ttu-id="85f50-390">**Vörunúmer:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="85f50-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="85f50-391">**Magn:** *20*</span><span class="sxs-lookup"><span data-stu-id="85f50-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="85f50-392">Sölupöntun lína 4:</span><span class="sxs-lookup"><span data-stu-id="85f50-392">Sales order line 4:</span></span>

        - <span data-ttu-id="85f50-393">**Vörunúmer:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="85f50-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="85f50-394">**Magn:** *40*</span><span class="sxs-lookup"><span data-stu-id="85f50-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="85f50-395">Sölupöntun lína 5:</span><span class="sxs-lookup"><span data-stu-id="85f50-395">Sales order line 5:</span></span>

        - <span data-ttu-id="85f50-396">**Vörunúmer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="85f50-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="85f50-397">**Magn:** *50*</span><span class="sxs-lookup"><span data-stu-id="85f50-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="85f50-398">Vörurnar og magnið sem er gefið upp hér er aðeins notað sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="85f50-399">Þær verða að hafa birgðir í tilgreindu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="85f50-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="85f50-400">Velja sölupöntunarlínu 1.</span><span class="sxs-lookup"><span data-stu-id="85f50-400">Select sales order line 1.</span></span> <span data-ttu-id="85f50-401">Því næst skal, í hlutanum **Sölupöntunarlína**, í valmyndinni **Birgðir**, velja **Frátekningar**.</span><span class="sxs-lookup"><span data-stu-id="85f50-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="85f50-402">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** og loka svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="85f50-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="85f50-403">Endurtakið skref 4 og 5 fyrir hverja sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="85f50-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="85f50-404">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="85f50-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="85f50-405">Eftirfarandi tilvik gerast:</span><span class="sxs-lookup"><span data-stu-id="85f50-405">The following events occur:</span></span>

    - <span data-ttu-id="85f50-406">Kerfið vinnur úr stofnaðri sendingu með því að nota sniðmátið sem felur í sér prentunarstig merkisins.</span><span class="sxs-lookup"><span data-stu-id="85f50-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="85f50-407">Útlit merkisins verður notað til að skilgreina snið merkisins og lokaniðurstaðan verður merki með fimm línum sem prentað er á prentara sem valinn er í sniðmáti merkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="85f50-408">Nýtt auðkenni farmbréfs er búið til fyrir sendingarnar.</span><span class="sxs-lookup"><span data-stu-id="85f50-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="85f50-409">Ef þú skilgreindir viðbætur númeraraðarinnar mun auðkenni bylgjumerkis fylgja **SSCC-18** númerasniðinu.</span><span class="sxs-lookup"><span data-stu-id="85f50-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="85f50-410">Hægt er að endurprenta þessi bylgjumerki með því að fara í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Ferill bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="85f50-411">Atburðarás 3: Prentun bylgjumerkis fyrir merki með mörg lög</span><span class="sxs-lookup"><span data-stu-id="85f50-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="85f50-412">Þessi atburðarás sýnir hvernig nota á prentunarvirkni bylgjumerkis þegar vöruhúsaferlin krefjast margra laga af merkimiðum.</span><span class="sxs-lookup"><span data-stu-id="85f50-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="85f50-413">Til dæmis gæti þurft að prenta sérstaka merkimiða fyrir kassa og bretti og hugsanlega þarf að prenta sundurliðunarmerki fyrir heila sendingu.</span><span class="sxs-lookup"><span data-stu-id="85f50-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="85f50-414">Sundurliðunarmerki eru sérstök gerð af merkimiða sem hægt er að nota til að skilja í sundur rúllur og gáma, t.d. merkimiða fyrir sendingarkennið og strikamerki, þannig að hægt sé að raða merkimiðunum auðveldlega eftir að þeir hafa verið prentaðir.</span><span class="sxs-lookup"><span data-stu-id="85f50-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="85f50-415">Helsti munurinn á skilgreiningu þessarar atburðarásar og skilgreiningar atburðarásar 1, fyrir utan þá staðreynd að sundurliðunarmerki eru virkjuð, er sá að margar gerðir bylgjumerkis verða að tengjast sniðmátum bylgjumerkja og línum röðunarflokkseininga.</span><span class="sxs-lookup"><span data-stu-id="85f50-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="85f50-416">Til að ná fram þessari skilgreiningu þarf að setja upp eftirfarandi þætti fyrir þessa atburðarás:</span><span class="sxs-lookup"><span data-stu-id="85f50-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="85f50-417">**Aðferðir bylgjuúrvinnslu:** Þú merkir aðferð bylgjumerkis sem „endurtakanleg,“ bætir henni tvisvar sinnum (eða oftar) við bylgjusniðmátið og stillir ólíka bylgjuskrefakóða.</span><span class="sxs-lookup"><span data-stu-id="85f50-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="85f50-418">**Sniðmát bylgjumerkja:** Þú skilgreinir sniðmát bylgjumerkja og tengir þau við bylgjusniðmátið.</span><span class="sxs-lookup"><span data-stu-id="85f50-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="85f50-419">Hvert sniðmát bylgjumerkis er með sína eigin gerð af bylgjumerki.</span><span class="sxs-lookup"><span data-stu-id="85f50-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="85f50-420">**Útlit bylgjumerkja:** Þú býrð til mörg útlit bylgjumerkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="85f50-421">Það verður sérstakt merkimiðaútlit fyrir hvert „lag“ af merkimiðum og það verður einnig útlit sundurliðunarmerkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="85f50-422">Þessi atburðarás sýnir verkflæðið frá upphafi til enda.</span><span class="sxs-lookup"><span data-stu-id="85f50-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="85f50-423">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="85f50-423">Make demo data available</span></span>

<span data-ttu-id="85f50-424">Til að fylgja þessari atburðarás verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann **USMF**.</span><span class="sxs-lookup"><span data-stu-id="85f50-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="85f50-425">Setja upp aðferð bylgjuúrvinnslu</span><span class="sxs-lookup"><span data-stu-id="85f50-425">Set up a wave process method</span></span>

1. <span data-ttu-id="85f50-426">Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.</span><span class="sxs-lookup"><span data-stu-id="85f50-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="85f50-427">Staðfestu að **waveLabelPrinting** sé á listanum.</span><span class="sxs-lookup"><span data-stu-id="85f50-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="85f50-428">Ef svo er ekki skal velja **Endurgera aðferðir** á aðgerðasvæðinu til að bæta því við.</span><span class="sxs-lookup"><span data-stu-id="85f50-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="85f50-429">Fyrir aðferðina **waveLabelPrinting** skal velja gátreitinn **Gera aðferð þannig að unnt sé að endurtaka hana**.</span><span class="sxs-lookup"><span data-stu-id="85f50-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="85f50-430">Velja bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="85f50-430">Set up a wave template</span></span>

1. <span data-ttu-id="85f50-431">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="85f50-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="85f50-432">Veldu sniðmát, t.d. **62 Sjálfgefin sending**.</span><span class="sxs-lookup"><span data-stu-id="85f50-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="85f50-433">Í flýtiflipanum **Aðferðir** skal færa aðferðina **Prentun bylgjumerkis** í dálkinn **Valdar aðferðir**.</span><span class="sxs-lookup"><span data-stu-id="85f50-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="85f50-434">Í dálknum **Valdar aðferðir** skal úthluta gildi **Bylgjuskrefakóða**, t.d. *Kassi*, á aðferðina **Prentun bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="85f50-435">Frekari upplýsingar um bylgjuskrefakóða er að finna í [Kóðar bylgjuskrefs](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="85f50-436">Færið aðferðina **Prentun bylgjumerkis** yfir í dálkinn **Valdar aðferðir** í annað skiptið.</span><span class="sxs-lookup"><span data-stu-id="85f50-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="85f50-437">Í dálknum **Valdar aðferðir** skal úthluta öðru gildi **Bylgjuskrefakóða**, t.d. *Bretti*, á aðra aðferð **Prentun bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="85f50-438">Frekari upplýsingar um bylgjuskrefakóða er að finna í [Kóðar bylgjuskrefs](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="85f50-439">Stofna þrenns konar útlit bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="85f50-440">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Útlit bylgjumerkja**.</span><span class="sxs-lookup"><span data-stu-id="85f50-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="85f50-441">Búið til færslu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="85f50-442">**Útlitskenni merkis:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="85f50-443">**Lýsing:** *Pakki (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="85f50-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="85f50-444">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-445">Á aðgerðasvæðinu skal velja **Línustillingar bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="85f50-446">Síðan **Línustillingar bylgjumerkis** birtist.</span><span class="sxs-lookup"><span data-stu-id="85f50-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="85f50-447">Hér er hægt að skilgreina breytilega hluta merkingarinnar.</span><span class="sxs-lookup"><span data-stu-id="85f50-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="85f50-448">Bætið við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-449">**Línukenni:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="85f50-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="85f50-450">**Töfluheiti línu:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="85f50-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="85f50-451">**Upphafsstaða línu:** *0*</span><span class="sxs-lookup"><span data-stu-id="85f50-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="85f50-452">Þessi reitur skilgreinir lóðréttu stöðuna þar sem línan byrjar á merkimiðanum.</span><span class="sxs-lookup"><span data-stu-id="85f50-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="85f50-453">**Línuhæð:** *0*</span><span class="sxs-lookup"><span data-stu-id="85f50-453">**Row height:** *0*</span></span>

        <span data-ttu-id="85f50-454">Þessi reitur skilgreinir hæð hverrar línu (í punktum), í samræmi við ZPL-staðalinn.</span><span class="sxs-lookup"><span data-stu-id="85f50-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="85f50-455">Hæð línunnar er jákvæð fyrir lárétta merkimiða og neikvæð fyrir lóðrétta merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="85f50-456">Fyrst að það er aðeins ein lína í þessu dæmi, er hægt að stilla gildið á *0* (núll).</span><span class="sxs-lookup"><span data-stu-id="85f50-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="85f50-457">**Línur á síðu:** *1*</span><span class="sxs-lookup"><span data-stu-id="85f50-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="85f50-458">Þessi reitur skilgreinir fjölda lína sem hægt er að prenta á hvern merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="85f50-459">Þessi uppsetning leiðir til þess að aðskilinn ZPL-merkimiði er prentaður fyrir hverja færslu í töflu bylgjumerkja.</span><span class="sxs-lookup"><span data-stu-id="85f50-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="85f50-460">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="85f50-460">Close the page.</span></span>
1. <span data-ttu-id="85f50-461">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="85f50-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="85f50-462">Í svarglugga fyrirspurnarritils á flipanum **Svið** skal bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="85f50-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-463">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-464">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-465">**Svæði:** *Gerð vinnu*</span><span class="sxs-lookup"><span data-stu-id="85f50-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="85f50-466">**Skilyrði:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="85f50-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="85f50-467">Þessi fyrirspurn tryggir að aðeins vinnulínur af tiltektargerð verði prentaðar á merkimiðann, ekki vinnulínur frágangs.</span><span class="sxs-lookup"><span data-stu-id="85f50-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="85f50-468">Ef ætlunin er að geta prentað auðkenni farmbréfsins, skal í flipanum **Samtengingar** velja töfluna **Vinnulínur** og tengja töfluna **Sendingar** við það.</span><span class="sxs-lookup"><span data-stu-id="85f50-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="85f50-469">Lokið svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="85f50-470">Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**.</span><span class="sxs-lookup"><span data-stu-id="85f50-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="85f50-471">Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn kóða fyrir nauðsynlegan síðuhaus.</span><span class="sxs-lookup"><span data-stu-id="85f50-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="85f50-472">Ef til dæmis Zebra-prentari er notaður er hægt að nota eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="85f50-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="85f50-473">Í hlutanum **Hluti meginmáls**, í reitinn **Meginmál merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegt meginmál.</span><span class="sxs-lookup"><span data-stu-id="85f50-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="85f50-474">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="85f50-475">Í hlutanum **Hluti síðufóts**, í reitinn **Síðufótur merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðufót.</span><span class="sxs-lookup"><span data-stu-id="85f50-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="85f50-476">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="85f50-477">Þessi uppsetning prentar eitt eintak af hverjum merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="85f50-478">Ef þörf er á fleiri eintökum (til dæmis eitt eintak fyrir hverja hlið brettisins) skal stilla gildið **n** fyrir hlutann **\^PQn** í síðufætinum á þann fjölda eintaka sem þarf.</span><span class="sxs-lookup"><span data-stu-id="85f50-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="85f50-479">Til dæmis, til að prenta fjögur eintök af hverjum merkimiða skal gefa upp **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="85f50-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="85f50-480">Nú er fyrsti merkimiðinn tilbúinn til notkunar.</span><span class="sxs-lookup"><span data-stu-id="85f50-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="85f50-481">Búið til aðra útlitsfærslu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="85f50-482">**Útlitskenni merkis:** *Bretti*</span><span class="sxs-lookup"><span data-stu-id="85f50-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="85f50-483">**Lýsing:** *Bretti*</span><span class="sxs-lookup"><span data-stu-id="85f50-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="85f50-484">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-485">Á aðgerðasvæðinu skal velja **Línustillingar bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="85f50-486">Síðan **Línustillingar bylgjumerkis** birtist.</span><span class="sxs-lookup"><span data-stu-id="85f50-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="85f50-487">Hér er hægt að skilgreina breytilega hluta merkingarinnar.</span><span class="sxs-lookup"><span data-stu-id="85f50-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="85f50-488">Bætið við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-489">**Línukenni:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="85f50-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="85f50-490">**Töfluheiti línu:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="85f50-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="85f50-491">**Upphafsstaða línu:** *0*</span><span class="sxs-lookup"><span data-stu-id="85f50-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="85f50-492">Þessi reitur skilgreinir lóðréttu stöðuna þar sem línan byrjar á merkimiðanum.</span><span class="sxs-lookup"><span data-stu-id="85f50-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="85f50-493">**Línuhæð:** *0*</span><span class="sxs-lookup"><span data-stu-id="85f50-493">**Row height:** *0*</span></span>

        <span data-ttu-id="85f50-494">Þessi reitur skilgreinir hæð hverrar línu (í punktum), í samræmi við ZPL-staðalinn.</span><span class="sxs-lookup"><span data-stu-id="85f50-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="85f50-495">Hæð línunnar er jákvæð fyrir lárétta merkimiða og neikvæð fyrir lóðrétta merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="85f50-496">Fyrst að það er aðeins ein lína í þessu dæmi, er hægt að stilla gildið á *0* (núll).</span><span class="sxs-lookup"><span data-stu-id="85f50-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="85f50-497">**Línur á síðu:** *1*</span><span class="sxs-lookup"><span data-stu-id="85f50-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="85f50-498">Þessi reitur skilgreinir fjölda lína sem hægt er að prenta á hvern merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="85f50-499">Þessi uppsetning leiðir til þess að sérstakur ZPL-merkimiði er prentaður fyrir hverja færslu í töflu bylgjumerkja.</span><span class="sxs-lookup"><span data-stu-id="85f50-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="85f50-500">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="85f50-500">Close the page.</span></span>
1. <span data-ttu-id="85f50-501">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="85f50-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="85f50-502">Í svarglugga fyrirspurnarritils á flipanum **Svið** skal bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="85f50-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-503">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-504">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-505">**Svæði:** *Gerð vinnu*</span><span class="sxs-lookup"><span data-stu-id="85f50-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="85f50-506">**Skilyrði:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="85f50-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="85f50-507">Þessi fyrirspurn tryggir að aðeins vinnulínur af tiltektargerð verði prentaðar á merkimiðann, ekki vinnulínur frágangs.</span><span class="sxs-lookup"><span data-stu-id="85f50-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="85f50-508">Ef ætlunin er að geta prentað auðkenni farmbréfsins, skal í flipanum **Samtengingar** velja töfluna **Vinnulínur** og tengja töfluna **Sendingar** við það.</span><span class="sxs-lookup"><span data-stu-id="85f50-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="85f50-509">Lokið svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="85f50-510">Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**.</span><span class="sxs-lookup"><span data-stu-id="85f50-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="85f50-511">Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn kóða fyrir nauðsynlegan síðuhaus.</span><span class="sxs-lookup"><span data-stu-id="85f50-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="85f50-512">Ef til dæmis Zebra-prentari er notaður er hægt að nota eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="85f50-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="85f50-513">Í hlutanum **Hluti meginmáls**, í reitinn **Meginmál merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegt meginmál.</span><span class="sxs-lookup"><span data-stu-id="85f50-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="85f50-514">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="85f50-515">Í hlutanum **Hluti síðufóts**, í reitinn **Síðufótur merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðufót.</span><span class="sxs-lookup"><span data-stu-id="85f50-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="85f50-516">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="85f50-517">Þessi uppsetning prentar eitt eintak af hverjum merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="85f50-518">Ef þörf er á fleiri eintökum (til dæmis eitt eintak fyrir hverja hlið brettisins) skal stilla gildið **n** fyrir hlutann **\^PQn** í síðufætinum á þann fjölda eintaka sem þarf.</span><span class="sxs-lookup"><span data-stu-id="85f50-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="85f50-519">Til dæmis, til að prenta fjögur eintök af hverjum merkimiða skal gefa upp **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="85f50-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="85f50-520">Nú er næsti merkimiði tilbúinn til notkunar.</span><span class="sxs-lookup"><span data-stu-id="85f50-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="85f50-521">Búið til þriðju útlitsfærslu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="85f50-522">**Útlitskenni merkis:** *Sundurliðun*</span><span class="sxs-lookup"><span data-stu-id="85f50-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="85f50-523">**Lýsing:** *Sundurliðunarmerki*</span><span class="sxs-lookup"><span data-stu-id="85f50-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="85f50-524">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-525">Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**.</span><span class="sxs-lookup"><span data-stu-id="85f50-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="85f50-526">Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðuhaus.</span><span class="sxs-lookup"><span data-stu-id="85f50-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="85f50-527">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="85f50-528">Að þessu sinni er ekki þörf á meginmáli.</span><span class="sxs-lookup"><span data-stu-id="85f50-528">This time, no body is required.</span></span> <span data-ttu-id="85f50-529">Færið þess vegna nauðsynlegan texta inn í hlutann **Hluti síðufóts**.</span><span class="sxs-lookup"><span data-stu-id="85f50-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="85f50-530">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="85f50-531">Nú er þriðji merkimiðinn tilbúinn til notkunar.</span><span class="sxs-lookup"><span data-stu-id="85f50-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85f50-532">Þessi þriðji merkimiði er sundurliðunarmerki sem verður notað til að aðskilja rúllur.</span><span class="sxs-lookup"><span data-stu-id="85f50-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="85f50-533">Búa til tvær gerðir bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-533">Create two wave label types</span></span>

1. <span data-ttu-id="85f50-534">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Gerðir bylgjumerkja**.</span><span class="sxs-lookup"><span data-stu-id="85f50-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="85f50-535">Búið til færslu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="85f50-536">**Merkimiðagerð:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="85f50-537">**Lýsing:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="85f50-538">Búið til aðra færslu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="85f50-539">**Merkimiðagerð:** *Bretti*</span><span class="sxs-lookup"><span data-stu-id="85f50-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="85f50-540">**Lýsing:** *Bretti*</span><span class="sxs-lookup"><span data-stu-id="85f50-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="85f50-541">Setja upp röðunarflokka eininga</span><span class="sxs-lookup"><span data-stu-id="85f50-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="85f50-542">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Röðunarflokkar einingar**.</span><span class="sxs-lookup"><span data-stu-id="85f50-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="85f50-543">Veljið eða stofnið flokk **Ea Kassi PL**.</span><span class="sxs-lookup"><span data-stu-id="85f50-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="85f50-544">Fyrir línuna **Kassi** skal stilla reitinn **Gerð bylgjustigs** á *Kassi*.</span><span class="sxs-lookup"><span data-stu-id="85f50-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="85f50-545">Fyrir línuna **PL** skal stilla reitinn **Gerð bylgjustigs** á *Bretti*.</span><span class="sxs-lookup"><span data-stu-id="85f50-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="85f50-546">Stofna sniðmát bylgjumerkja</span><span class="sxs-lookup"><span data-stu-id="85f50-546">Create wave label templates</span></span>

1. <span data-ttu-id="85f50-547">Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Sniðmát bylgjumerkja**.</span><span class="sxs-lookup"><span data-stu-id="85f50-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="85f50-548">Stofna sniðmát merkimiða sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="85f50-549">**Heiti sniðmátsmerkis:** *Merkimiðar kassa*</span><span class="sxs-lookup"><span data-stu-id="85f50-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="85f50-550">**Lýsing:** *Merkimiðar kassa*</span><span class="sxs-lookup"><span data-stu-id="85f50-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="85f50-551">**Kóði bylgjuskrefs:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="85f50-552">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="85f50-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="85f50-553">Í flýtiflipanum **Almennt**, í reitnum **Gerð bylgjumerkis**, skal velja gildi á borð við *Kassi*.</span><span class="sxs-lookup"><span data-stu-id="85f50-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="85f50-554">Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal bæta við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-555">**Útlitskenni merkis:** *Pakki*</span><span class="sxs-lookup"><span data-stu-id="85f50-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="85f50-556">**Heiti prentara:** Veljið viðeigandi ZPL-prentara.</span><span class="sxs-lookup"><span data-stu-id="85f50-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="85f50-557">**Keyra fyrirspurn:** *Já* (Þessi stilling er valfrjáls, en mælt er með henni til að hámarka afköst.)</span><span class="sxs-lookup"><span data-stu-id="85f50-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="85f50-558">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-559">Valfrjálst: Ef verið er að setja upp merkimiða sem hannaður er með ákveðinn viðskiptavin í huga, þarf að búa til fyrirspurn til að finna lykil viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="85f50-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="85f50-560">Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="85f50-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="85f50-561">Því næst, í svarglugga fyrirspurnarritils í flipanum **Svið**, skal bæta við línu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-562">**Tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="85f50-563">**Afleidd tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="85f50-564">**Reitur:** *Reikningsnúmer*</span><span class="sxs-lookup"><span data-stu-id="85f50-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="85f50-565">**Skilyrði:** Sláið inn viðeigandi númer viðskiptavinalykils.</span><span class="sxs-lookup"><span data-stu-id="85f50-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="85f50-566">Þegar því er lokið skal velja **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="85f50-567">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils fyrir allt merkjasniðmát.</span><span class="sxs-lookup"><span data-stu-id="85f50-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="85f50-568">Í svarglugga fyrirspurnarritils, í flipanum **Röðun**, skal bæta við línu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-569">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-570">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-571">**Reitur:** *Tilvísunarkenni hleðslulínu (færslukenni)*</span><span class="sxs-lookup"><span data-stu-id="85f50-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="85f50-572">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="85f50-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="85f50-573">Bætið við annarri línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-574">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-575">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-576">**Reitur:** *Auðkenni sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="85f50-577">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="85f50-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="85f50-578">Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="85f50-579">Skilaboðagluggi biður um að endurstillingaraðgerð flokkunar verði staðfest.</span><span class="sxs-lookup"><span data-stu-id="85f50-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="85f50-580">Veldu **Já** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="85f50-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="85f50-581">Á aðgerðasvæðinu skal velja **Sniðmátsflokkur bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="85f50-582">Í svarglugganum **Sniðmátsflokkur bylgjumerkis**, fyrir línuna þar sem reiturinn **Heiti tilvísunarreits** er stilltur á *Auðkenni sendingar*, skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="85f50-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="85f50-583">**Prenta sundurliðunarmerki:** Veljið þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="85f50-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="85f50-584">**Útlitskenni merkis:** Veljið sundurliðunarmerki.</span><span class="sxs-lookup"><span data-stu-id="85f50-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="85f50-585">(Til dæmis velja merkjaútlitið *Sundurliðun* sem búið var til fyrr í þessari atburðarás.)</span><span class="sxs-lookup"><span data-stu-id="85f50-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="85f50-586">**Heiti prentara:** Veljið prentarann fyrir sundurliðunarmerkið.</span><span class="sxs-lookup"><span data-stu-id="85f50-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="85f50-587">(Venjulega, í þeim tilgangi að skipta niður merkimiðarúllum, ætti að velja sama prentarann og er valinn í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="85f50-588">Hins vegar eru aðrar atburðarásir mögulegar.)</span><span class="sxs-lookup"><span data-stu-id="85f50-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="85f50-589">Fyrir línuna þar sem reiturinn **Heiti tilvísunarreits** er stillt á *Tilvísunarkenni hleðslulínu* skal velja gátreitinn **Smíðakenni merkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85f50-590">Þessi uppsetning býr til eina merkimiðaröð („Kassi 1 af X“) fyrir hverja hleðslulínu í gegnum bylgjuna, óháð uppsetningu vinnuflokkunar.</span><span class="sxs-lookup"><span data-stu-id="85f50-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="85f50-591">Hægt er að prenta þessa númeraröð merkimiða á útlit merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="85f50-592">Að auki verða merkimiðar fyrir mismunandi sendingar aðskildir með völdum sundurliðunarmiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="85f50-593">Smellið á **Í lagi** til að loka svarglugganum **Sniðmátsflokkur bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="85f50-594">Búið til annað sniðmát merkimiða sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="85f50-595">**Heiti á sniðmáti merkis:** *Brettamiðar*</span><span class="sxs-lookup"><span data-stu-id="85f50-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="85f50-596">**Lýsing:** *Merkimiðar brettis*</span><span class="sxs-lookup"><span data-stu-id="85f50-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="85f50-597">**Kóði bylgjuskrefs:** *Bretti*</span><span class="sxs-lookup"><span data-stu-id="85f50-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="85f50-598">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="85f50-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="85f50-599">Í flýtiflipanum **Almennt**, í reitnum **Gerð bylgjumerkis**, skal velja gildi á borð við *Bretti*.</span><span class="sxs-lookup"><span data-stu-id="85f50-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="85f50-600">Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal bæta við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-601">**Útlitskenni merkis:** *Bretti*</span><span class="sxs-lookup"><span data-stu-id="85f50-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="85f50-602">**Heiti prentara:** Veljið viðeigandi ZPL-prentara.</span><span class="sxs-lookup"><span data-stu-id="85f50-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="85f50-603">**Keyra fyrirspurn:** *Já* (Þessi stilling er valfrjáls, en mælt er með henni til að hámarka afköst.)</span><span class="sxs-lookup"><span data-stu-id="85f50-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="85f50-604">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="85f50-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f50-605">Valfrjálst: Ef verið er að setja upp merkimiða sem hannaður er með ákveðinn viðskiptavin í huga, þarf að búa til fyrirspurn til að finna lykil viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="85f50-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="85f50-606">Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="85f50-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="85f50-607">Því næst, í svarglugga fyrirspurnarritils í flipanum **Svið**, skal bæta við línu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-608">**Tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="85f50-609">**Afleidd tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="85f50-610">**Reitur:** *Reikningsnúmer*</span><span class="sxs-lookup"><span data-stu-id="85f50-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="85f50-611">**Skilyrði:** Sláið inn viðeigandi númer viðskiptavinalykils.</span><span class="sxs-lookup"><span data-stu-id="85f50-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="85f50-612">Þegar því er lokið skal velja **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="85f50-613">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils fyrir allt merkjasniðmát.</span><span class="sxs-lookup"><span data-stu-id="85f50-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="85f50-614">Í svarglugga fyrirspurnarritils, í flipanum **Röðun**, skal bæta við línu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-615">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-616">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-617">**Reitur:** *Tilvísunarkenni hleðslulínu (færslukenni)*</span><span class="sxs-lookup"><span data-stu-id="85f50-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="85f50-618">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="85f50-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="85f50-619">Bætið við annarri línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="85f50-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="85f50-620">**Tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-621">**Afleidd tafla:** *Vinnulínur*</span><span class="sxs-lookup"><span data-stu-id="85f50-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="85f50-622">**Reitur:** *Auðkenni sendingar*</span><span class="sxs-lookup"><span data-stu-id="85f50-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="85f50-623">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="85f50-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="85f50-624">Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="85f50-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="85f50-625">Skilaboðagluggi biður um að endurstillingaraðgerð flokkunar verði staðfest.</span><span class="sxs-lookup"><span data-stu-id="85f50-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="85f50-626">Veldu **Já** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="85f50-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="85f50-627">Á aðgerðasvæðinu skal velja **Sniðmátsflokkur bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="85f50-628">Í svarglugganum **Sniðmátsflokkur bylgjumerkis**, fyrir línuna þar sem reiturinn **Heiti tilvísunarreits** er stilltur á *Auðkenni sendingar*, skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="85f50-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="85f50-629">**Prenta sundurliðunarmerki:** Veljið þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="85f50-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="85f50-630">**Útlitskenni merkis:** Veljið sundurliðunarmerki.</span><span class="sxs-lookup"><span data-stu-id="85f50-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="85f50-631">(Til dæmis velja merkjaútlitið *Sundurliðun* sem búið var til fyrr í þessari atburðarás.)</span><span class="sxs-lookup"><span data-stu-id="85f50-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="85f50-632">**Heiti prentara:** Veljið prentarann fyrir sundurliðunarmerkið.</span><span class="sxs-lookup"><span data-stu-id="85f50-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="85f50-633">(Venjulega, í þeim tilgangi að skipta niður merkimiðarúllum, ætti að velja sama prentarann og er valinn í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="85f50-634">Hins vegar eru aðrar atburðarásir mögulegar.)</span><span class="sxs-lookup"><span data-stu-id="85f50-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="85f50-635">Fyrir línuna þar sem reiturinn **Heiti tilvísunarreits** er stillt á *Tilvísunarkenni hleðslulínu* skal velja gátreitinn **Smíðakenni merkis**.</span><span class="sxs-lookup"><span data-stu-id="85f50-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85f50-636">Þessi uppsetning býr til eina merkimiðaröð („Kassi 1 af X“) fyrir hverja hleðslulínu í gegnum bylgjuna, óháð uppsetningu vinnuflokkunar.</span><span class="sxs-lookup"><span data-stu-id="85f50-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="85f50-637">Hægt er að prenta þessa númeraröð merkimiða á útlit merkimiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="85f50-638">Að auki verða merkimiðar fyrir mismunandi sendingar aðskildir með völdum sundurliðunarmiða.</span><span class="sxs-lookup"><span data-stu-id="85f50-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="85f50-639">Skilgreina viðbætur númeraraðar</span><span class="sxs-lookup"><span data-stu-id="85f50-639">Configure number sequence extensions</span></span>

<span data-ttu-id="85f50-640">Viðbætur númeraraðar stjórna GS1-reglufylgni tiltekinna númeraraða.</span><span class="sxs-lookup"><span data-stu-id="85f50-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="85f50-641">Þessi skilgreining er valfrjáls fyrir núverandi atburðarás.</span><span class="sxs-lookup"><span data-stu-id="85f50-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="85f50-642">Nánari upplýsingar og leiðbeiningar um skilgreiningar er að finna í [Skilgreina viðbætur númeraraðar](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="85f50-643">Stofna sölupöntun og losa hana í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="85f50-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="85f50-644">Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="85f50-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="85f50-645">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="85f50-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="85f50-646">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="85f50-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="85f50-647">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="85f50-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="85f50-648">Bæta við tveimur sölupöntunarlínum:</span><span class="sxs-lookup"><span data-stu-id="85f50-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="85f50-649">Sölupöntun lína 1:</span><span class="sxs-lookup"><span data-stu-id="85f50-649">Sales order line 1:</span></span>

        - <span data-ttu-id="85f50-650">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="85f50-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="85f50-651">**Magn:** *9024*</span><span class="sxs-lookup"><span data-stu-id="85f50-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="85f50-652">**Eining:** *ea* (9024 ea = 376 Kassi = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="85f50-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="85f50-653">Sölupöntun lína 2:</span><span class="sxs-lookup"><span data-stu-id="85f50-653">Sales order line 2:</span></span>

        - <span data-ttu-id="85f50-654">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="85f50-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="85f50-655">**Magn:** *9016*</span><span class="sxs-lookup"><span data-stu-id="85f50-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="85f50-656">**Eining:** *ea* (9016 ea = 322 Kassi = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="85f50-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="85f50-657">Vörurnar og magnið sem er gefið upp hér er aðeins notað sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="85f50-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="85f50-658">Nota verður röðunarflokk einingar sem var skilgreindur áður, viðeigandi umreikninga eininga úr *ea* í *Kassi* í *PL* verður að vera skilgreint fyrir þær og þær að vera með birgðastöðu í vöruhúsi *62*.</span><span class="sxs-lookup"><span data-stu-id="85f50-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="85f50-659">Frekari upplýsingar er að finna í [Mælieining og birgðareglur](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="85f50-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="85f50-660">Velja sölupöntunarlínu 1.</span><span class="sxs-lookup"><span data-stu-id="85f50-660">Select sales order line 1.</span></span> <span data-ttu-id="85f50-661">Því næst skal, í hlutanum **Sölupöntunarlína**, í valmyndinni **Birgðir**, velja **Frátekningar**.</span><span class="sxs-lookup"><span data-stu-id="85f50-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="85f50-662">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** og loka svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="85f50-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="85f50-663">Endurtakið skref 4 og 5 fyrir sölupöntunarlínu 2.</span><span class="sxs-lookup"><span data-stu-id="85f50-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="85f50-664">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="85f50-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="85f50-665">Eftirfarandi tilvik gerast:</span><span class="sxs-lookup"><span data-stu-id="85f50-665">The following events occur:</span></span> 

    - <span data-ttu-id="85f50-666">Kerfið vinnur úr stofnaðri sendingu með því að nota sniðmátið sem felur í sér prentunarstig merkisins.</span><span class="sxs-lookup"><span data-stu-id="85f50-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="85f50-667">Útlit merkisins verður notað til að skilgreina snið merkisins og niðurstaðan verður merki sem prentað er á prentara sem valinn er í sniðmáti merkis.</span><span class="sxs-lookup"><span data-stu-id="85f50-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="85f50-668">Bylgjumerki eru búin til og prentuð.</span><span class="sxs-lookup"><span data-stu-id="85f50-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="85f50-669">Fjöldi merkimiða verður sá sami og kassafjöldinn (í þessu dæmi, 376 kassamerki fyrir línu 1 og 322 kassamerki fyrir línu 2, 47 PL-miðar fyrir línu 1, 47 PL-miðar fyrir línu 2 og tveir sundurliðunarmiðar sem eru með auðkenni sendingarinnar).</span><span class="sxs-lookup"><span data-stu-id="85f50-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="85f50-670">Nýtt auðkenni farmbréfs er búið til fyrir sendingarnar.</span><span class="sxs-lookup"><span data-stu-id="85f50-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="85f50-671">Ef þú skilgreindir viðbætur númeraraðarinnar mun auðkenni bylgjumerkis fylgja **SSCC-18** númerasniðinu.</span><span class="sxs-lookup"><span data-stu-id="85f50-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="85f50-672">Hægt er að skoða og endurprenta bylgjumerki á eftirfarandi síðum:</span><span class="sxs-lookup"><span data-stu-id="85f50-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="85f50-673">Allar sendingar \> Upplýsingar sendingar</span><span class="sxs-lookup"><span data-stu-id="85f50-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="85f50-674">Allar hleðslur \> Upplýsingar um hleðslu</span><span class="sxs-lookup"><span data-stu-id="85f50-674">All loads \> Load details</span></span>
- <span data-ttu-id="85f50-675">Allar bylgjur</span><span class="sxs-lookup"><span data-stu-id="85f50-675">All waves</span></span>
- <span data-ttu-id="85f50-676">Bylgjumerki</span><span class="sxs-lookup"><span data-stu-id="85f50-676">Wave labels</span></span>
- <span data-ttu-id="85f50-677">Ferill bylgjumerkis</span><span class="sxs-lookup"><span data-stu-id="85f50-677">Wave label history</span></span>

<span data-ttu-id="85f50-678">Fyrir flestar af þessum síðum er hægt að finna viðeigandi virkni með því að velja **Bylgjumerki** í flokknum **Tengdar upplýsingar** í flipanum **Sendingar** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="85f50-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]