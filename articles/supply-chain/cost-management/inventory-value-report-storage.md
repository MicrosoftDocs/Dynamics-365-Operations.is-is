---
title: Skýrsla um birgðavirði í geymslu
description: Þetta efnisatriði útskýrir hvernig á að keyra skýrslu um birgðarvirði í geymslu og gera úttakið aðgengilegt stafrænt, annað hvort sem gagnvirka síðu í Microsoft Dynamics 365 Supply Chain Management eða á skjali sem hægt er að flytja út á nokkrum sniðum.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 03426e86186c6aa283531eb37ae26527e6891042
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276926"
---
# <a name="inventory-value-storage-report"></a><span data-ttu-id="2afed-103">Skýrsla um birgðavirði í geymslu</span><span class="sxs-lookup"><span data-stu-id="2afed-103">Inventory value storage report</span></span>

<span data-ttu-id="2afed-104">Þetta efnisatriði útskýrir hvernig á að keyra **Skýrslu um birgðarvirði í geymslu** og gera úttakið aðgengilegt stafrænt, annað hvort sem gagnvirka síðu í Microsoft Dynamics 365 Supply Chain Management eða á skjali sem hægt er að flytja út á nokkrum sniðum.</span><span class="sxs-lookup"><span data-stu-id="2afed-104">This topic explains how to run an **Inventory value storage** report and make the output available digitally, either as an interactive page in Microsoft Dynamics 365 Supply Chain Management or as an exported document in any of several formats.</span></span>

<span data-ttu-id="2afed-105">Þegar þú skoðar skýrsluna í vafranum þínum eru dálkar og samanlagðri stöðu er breytt á kvikan hátt, miðað við skipulagið sem þú hefur grunnstillt.</span><span class="sxs-lookup"><span data-stu-id="2afed-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on the layout that you've configured.</span></span> <span data-ttu-id="2afed-106">Þú getur flokkað niðurstöðurnar, síað þær, borað niður í gögnin og fleira.</span><span class="sxs-lookup"><span data-stu-id="2afed-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="2afed-107">Niðurstöður skýrslunnar eru vistaðar í gagnaeiningu **Birgðavirðis**.</span><span class="sxs-lookup"><span data-stu-id="2afed-107">Report results are stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="2afed-108">Þar af leiðandi getur þú síað og flutt niðurstöðurnar út á sniði eins og á CSV-skrá eða Microsoft Excel-sniði.</span><span class="sxs-lookup"><span data-stu-id="2afed-108">Therefore, you can filter and export the results to a format such as comma-separated values (CSV) or Microsoft Excel format.</span></span>

<span data-ttu-id="2afed-109">**Skýrsla um birgðavirði í geymslu** er gagnleg þegar úttakið inniheldur margar línur.</span><span class="sxs-lookup"><span data-stu-id="2afed-109">The **Inventory value storage** report is helpful when the output contains many lines.</span></span> <span data-ttu-id="2afed-110">Til dæmis hefur þú 50.000 vörur og 300 verslanir hafa verið stofnaðar sem vöruhús.</span><span class="sxs-lookup"><span data-stu-id="2afed-110">For example, you have 50,000 items, and 300 stores have been created as warehouses.</span></span> <span data-ttu-id="2afed-111">Í þessu tilfelli, ef þú biður um lokastöður birgða eftir vöru, síðu og vöruhúsi, mun úttakið innihalda margar línur.</span><span class="sxs-lookup"><span data-stu-id="2afed-111">In this case, if you request inventory ending balances by item, site, and warehouse, the output will contain many lines.</span></span>

> [!NOTE]
> <span data-ttu-id="2afed-112">Skýrslan mun ekki innihalda millisamtölur sem eru skilgreind í útliti skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="2afed-112">The report won't include subtotals that are defined in the report layout.</span></span> <span data-ttu-id="2afed-113">Hún mun heldur ekki fela í sér fjárhagsstöður, jafnvel ekki þegar þær eru skilgreindar í útliti skýrslu.</span><span class="sxs-lookup"><span data-stu-id="2afed-113">It also won't include general ledger balances, even when they are defined in the report layout.</span></span> <span data-ttu-id="2afed-114">Afstemming við Fjárhag verður að fara fram með því að nota prófjöfnuð.</span><span class="sxs-lookup"><span data-stu-id="2afed-114">Reconciliation to the general ledger must be done by using trial balances.</span></span>

## <a name="turn-on-the-inventory-value-storage-feature"></a><span data-ttu-id="2afed-115">Kveikja á eiginleikanum fyrir birgðavirði í geymslu</span><span class="sxs-lookup"><span data-stu-id="2afed-115">Turn on the Inventory value storage feature</span></span>

<span data-ttu-id="2afed-116">Áður en þú getur útbúið skýrslu fyrir **Birgðarvirði í geymslu** verður þú að kveikja á eiginleikanum í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="2afed-116">Before you can generate an **Inventory value storage** report, you must turn on the feature in your system.</span></span> <span data-ttu-id="2afed-117">Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="2afed-117">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2afed-118">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="2afed-118">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2afed-119">**Eining** – Kostnaðarstjórnun</span><span class="sxs-lookup"><span data-stu-id="2afed-119">**Module** – Cost management</span></span>
- <span data-ttu-id="2afed-120">**Heiti eiginleika** – Birgðarvirði í geymslu</span><span class="sxs-lookup"><span data-stu-id="2afed-120">**Feature name** – Inventory value storage</span></span>

## <a name="generate-an-inventory-value-storage-report"></a><span data-ttu-id="2afed-121">Búa til skýrslu um birgðarvirði í geymslu</span><span class="sxs-lookup"><span data-stu-id="2afed-121">Generate an Inventory value storage report</span></span>

<span data-ttu-id="2afed-122">Fylgdu þessum skrefum til að búa til og geyma skýrslu um **Birgðarvirði í geymslu**.</span><span class="sxs-lookup"><span data-stu-id="2afed-122">Follow these steps to generate and store an **Inventory value storage** report.</span></span>

1. <span data-ttu-id="2afed-123">Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla skýrslu fyrir birgðavirði í geymslu**.</span><span class="sxs-lookup"><span data-stu-id="2afed-123">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="2afed-124">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="2afed-124">Select **New**.</span></span>
1. <span data-ttu-id="2afed-125">Í valmyndinni **Birgðavirði** sem birtist skaltu stilla eftirfarandi gildi til að skilgreina hvaða skrár skal taka með í skýrslunni:</span><span class="sxs-lookup"><span data-stu-id="2afed-125">In the **Inventory value** dialog box that appears, set the following values to define which records are included in your report:</span></span>

    - <span data-ttu-id="2afed-126">Sláðu inn einkvæmt heiti skýrslunnar í flýtiflipanum **Færibreytur** og notaðu svæðin í hlutanum **Dagsetningabil** til að skilgreina hvaða skrár eru teknar með í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="2afed-126">On the **Parameters** FastTab, enter a unique name for the report, and use the fields in the **Date interval** section to define which records are included in the report.</span></span> <span data-ttu-id="2afed-127">Til að tilgreina dagsetningabilið geturðu annað hvort valið forstillt svið (miðað við hvenær skýrslan var búin til) í svæðinu **Kóði dagsetningabils** eða valið ákveðin dagsetningar í reitunum **Frá dagsetningu** og **Til dagsetningar**.</span><span class="sxs-lookup"><span data-stu-id="2afed-127">To define the date interval, you can either select a preset range (relative to the report generation date) in the **Date interval code** field, or select specific dates in the **From date** and **To date** fields.</span></span> <!-- KFM: What is the ID setting for here? What do its values mean? -->
    - <span data-ttu-id="2afed-128">Á flýtiflipanum **Færslur til að taka með** skaltu setja upp síur og takmarkanir til að skilgreina hvaða gögn á að taka með í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="2afed-128">On the **Records to include** FastTab, set up filters and constraints to define which data is included in the report.</span></span>
    - <span data-ttu-id="2afed-129">Á flýtiflipanum **Keyra í bakgrunni** skaltu tilgreina hvernig, hvenær og hversu oft á að búa skýrsluna til.</span><span class="sxs-lookup"><span data-stu-id="2afed-129">On the **Run in the background** FastTab, specify how, when, and how often the report is generated.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2afed-130">Þessi skýrsla er alltaf keyrð sem hluti af runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="2afed-130">This report is always run as part of a batch job.</span></span>

1. <span data-ttu-id="2afed-131">Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="2afed-131">Select **OK** to apply your settings and close the dialog box.</span></span>

<span data-ttu-id="2afed-132">Eftir að runuvinnslunni er lokið birtist skýrslan á síðu **Skýrslu um birgðarvirði í geymslu**.</span><span class="sxs-lookup"><span data-stu-id="2afed-132">After the batch job is completed, the report will be listed on the **Inventory value report storage** page.</span></span> <span data-ttu-id="2afed-133">Hugsanlega verður að endurhlaða síðuna til að skýrslan birtist.</span><span class="sxs-lookup"><span data-stu-id="2afed-133">You might have to refresh the page to see the report.</span></span>

## <a name="explore-an-inventory-value-storage-report"></a><span data-ttu-id="2afed-134">Skoða skýrslu um birgðarvirði í geymslu</span><span class="sxs-lookup"><span data-stu-id="2afed-134">Explore an Inventory value storage report</span></span>

<span data-ttu-id="2afed-135">Eftir að þú hefur búið til skýrslu geturðu opnað og skoðað hana hvenær sem er með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2afed-135">After you've generated a report, you can view and explore it at any time by following these steps.</span></span>

1. <span data-ttu-id="2afed-136">Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla skýrslu fyrir birgðavirði í geymslu**.</span><span class="sxs-lookup"><span data-stu-id="2afed-136">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="2afed-137">Veldu skýrslu á listanum.</span><span class="sxs-lookup"><span data-stu-id="2afed-137">Select a report in the list.</span></span>
1. <span data-ttu-id="2afed-138">Veldu **Skoða upplýsingar** til að sýna efni skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="2afed-138">Select **View details** to show the report content.</span></span>
1. <span data-ttu-id="2afed-139">Skoðaðu skýrsluna með því að fylgja einhverjum af þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2afed-139">Explore the report by following any of these steps:</span></span>

    - <span data-ttu-id="2afed-140">Eins og á við um flestar staðlaðar síður í Supply Chain Management geturðu valið næstum hvaða dálk sem er til að raða eða sía hnitanetið eftir gildunum í þeim dálki.</span><span class="sxs-lookup"><span data-stu-id="2afed-140">As for most standard pages in Supply Chain Management, you can select almost any column heading to sort or filter the grid by the values in that column.</span></span>
    - <span data-ttu-id="2afed-141">Notaðu svæðið **Sía** til að sía skýrsluna eftir hvaða gildi sem er í nokkrum tiltækum dálkum.</span><span class="sxs-lookup"><span data-stu-id="2afed-141">Use the **Filter** field to filter the report by any value in any of several available columns.</span></span>
    - <span data-ttu-id="2afed-142">Notaðu valmyndina Skoða (fyrir ofan svæðið **Sía**) til að vista og hlaða inn eftirlætis samsetningum flokkunar- og síuvalkosta.</span><span class="sxs-lookup"><span data-stu-id="2afed-142">Use the view menu (above the **Filter** field) to save and load your favorite combinations of sort and filter options.</span></span>

## <a name="export-an-inventory-value-storage-report"></a><span data-ttu-id="2afed-143">Flytja út skýrslu um birgðarvirði í geymslu</span><span class="sxs-lookup"><span data-stu-id="2afed-143">Export an Inventory value storage report</span></span>

<span data-ttu-id="2afed-144">Hver skýrsla sem þú býrð til er geymd í gagnaeiningunni **Birgðavirði**.</span><span class="sxs-lookup"><span data-stu-id="2afed-144">Every report that you generate is stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="2afed-145">Þú getur notað staðlaða eiginleika gagnastjórnunar fyrir Supply Chain Management til að flytja út gögn frá þessari einingu til allra studdra gagnasniða, eins og CSV- eða Excel-sniða.</span><span class="sxs-lookup"><span data-stu-id="2afed-145">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, such as CSV or Excel format.</span></span>

<span data-ttu-id="2afed-146">Eftirfarandi dæmi sýnir hvernig á að flytja út skýrslu um **birgðarvirði í geymslu**.</span><span class="sxs-lookup"><span data-stu-id="2afed-146">The following example shows how to export an **Inventory value report** report.</span></span>

1. <span data-ttu-id="2afed-147">Opnaðu **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="2afed-147">Go to **System administration \> Workspaces \> Data management**.</span></span>
1. <span data-ttu-id="2afed-148">Í hlutanum **Flytja inn / Flytja út** velurðu reitinn **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="2afed-148">In the **Import / Export** section, select the **Export** tile.</span></span> 
1. <span data-ttu-id="2afed-149">Á síðunni **Útflutningur** sem birtist seturðu upp útflutningsverkið.</span><span class="sxs-lookup"><span data-stu-id="2afed-149">On the **Export** page that appears, you will set up the export job.</span></span> <span data-ttu-id="2afed-150">Færið fyrst inn heiti hóps fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="2afed-150">First enter a group name for the job.</span></span>
1. <span data-ttu-id="2afed-151">Í hlutanum **Valdar einingar** velurðu **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="2afed-151">In the **Selected entities** section, select **Add entity**.</span></span>
1. <span data-ttu-id="2afed-152">Í svarglugganum sem birtist, skal velja eitt af eftirfarandi svæðum:</span><span class="sxs-lookup"><span data-stu-id="2afed-152">In the dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="2afed-153">**Heiti einingar** – Veldu **Birgðarvirði**.</span><span class="sxs-lookup"><span data-stu-id="2afed-153">**Entity name** – Select **Inventory value**.</span></span>
    - <span data-ttu-id="2afed-154">**Markmiðsgagnasnið** - Veldu sniðið sem á að flytja gögn út á.</span><span class="sxs-lookup"><span data-stu-id="2afed-154">**Target data format** – Select the format to export data to.</span></span>

1. <span data-ttu-id="2afed-155">Smelltu á **Bæta við** til að bæta við nýju línunni og smelltu síðan á **Loka** til að loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="2afed-155">Select **Add** to add the new row, and then select **Close** to close the dialog box.</span></span>
1. <span data-ttu-id="2afed-156">Venjulega muntu flytja út eina skýrslu í einu.</span><span class="sxs-lookup"><span data-stu-id="2afed-156">Usually, you will export one report at a time.</span></span> <span data-ttu-id="2afed-157">Til að flytja út eina skýrslu skaltu setja upp síu fyrir línuna sem þú varst að bæta við í svarglugganum **Fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="2afed-157">To export a single report, set up a filter for the row that you just added to the **Inquiry** dialog box.</span></span> <span data-ttu-id="2afed-158">Á þennan hátt geturðu skilgreint hvaða skýrslu frá einingunni **Birgðavirði** er innifalinn í útflutningi þínum.</span><span class="sxs-lookup"><span data-stu-id="2afed-158">In this way, you can define which report from the **Inventory value** entity is included in your export.</span></span> <span data-ttu-id="2afed-159">Fylgdu þessum skrefum til að stilla eftirfarandi síuvalkosti til að flytja út eina skýrslu:</span><span class="sxs-lookup"><span data-stu-id="2afed-159">Follow these steps to set the following filter options to export a single report:</span></span>

    1. <span data-ttu-id="2afed-160">Veldu **Bæta við** til að bæta við röð á flipanum **Svið**.</span><span class="sxs-lookup"><span data-stu-id="2afed-160">On the **Range** tab, select **Add** to add a row.</span></span>
    2. <span data-ttu-id="2afed-161">Stilltu svæðið **Tafla** á **Birgðavirði**.</span><span class="sxs-lookup"><span data-stu-id="2afed-161">Set the **Table** field to **Inventory value**.</span></span>
    3. <span data-ttu-id="2afed-162">Stilltu svæðið **Afleidd tafla** á **Birgðavirði**.</span><span class="sxs-lookup"><span data-stu-id="2afed-162">Set the **Derived table** field to **Inventory value**.</span></span>
    4. <span data-ttu-id="2afed-163">Stilltu svæðið **Svæði** á svæðið sem þú vilt sía eftir.</span><span class="sxs-lookup"><span data-stu-id="2afed-163">Set the **Field** field to the field that you want to filter by.</span></span> <span data-ttu-id="2afed-164">Yfirleitt notarðu svæðið **Keyrsluheiti** og/eða svæðið **Keyrslutími**.</span><span class="sxs-lookup"><span data-stu-id="2afed-164">Usually, you will use the **Execution name** field and/or the **Execution time** field.</span></span>
    5. <span data-ttu-id="2afed-165">Stilltu svæðið **Skilyrði** á gildi sem þú vilt leita að í valda svæðinu.</span><span class="sxs-lookup"><span data-stu-id="2afed-165">Set the **Criteria** field to the value that you want to look for in the selected field.</span></span> <span data-ttu-id="2afed-166">(Ef þú valdir svæðið **Keyrsluheiti** í fyrra skrefi verður þetta gildi heiti skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="2afed-166">(If you selected the **Execution name** field in the previous step, this value will be the name of the report.</span></span> <span data-ttu-id="2afed-167">Ef þú valdir svæðið **Keyrslutími** verður það tíminn sem skýrslan var búin til.)</span><span class="sxs-lookup"><span data-stu-id="2afed-167">If you selected the **Execution time** field, it will be the time when the report was generated.)</span></span>
    6. <span data-ttu-id="2afed-168">Bættu við eins mörgum línum við flipann **Svið** eins og þú þarft, þar til þú hefur borið einkvæm kennsl á skýrsluna sem þú ert að leita að.</span><span class="sxs-lookup"><span data-stu-id="2afed-168">Add more rows to the **Range** tab as you require, until you've uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="2afed-169">Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="2afed-169">Select **OK** to save your settings and close the dialog box.</span></span>
1. <span data-ttu-id="2afed-170">Veldu **Vista** til að vista uppsetningu á útflutningi.</span><span class="sxs-lookup"><span data-stu-id="2afed-170">Select **Save** to save your export setup.</span></span>
1. <span data-ttu-id="2afed-171">Á flipanum **Valkostir útflutnings** velurðu **Flytja út núna** til að búa til útflutningsskrána.</span><span class="sxs-lookup"><span data-stu-id="2afed-171">On the **Export options** tab, select **Export now** to generate the export file.</span></span>
1. <span data-ttu-id="2afed-172">Á **Yfirlitssíðu keyrslu** sem birtist geturðu skoðað stöðu útflutningsverksins þíns og lista yfir allar einingar sem voru fluttar út.</span><span class="sxs-lookup"><span data-stu-id="2afed-172">On the **Execution summary** page that appears, you can view the status of your export job and a list of the entities that were exported.</span></span> <span data-ttu-id="2afed-173">Í hlutanum**Vinnslustaða einingar** velurðu **Birgðavirði** á listanum og smellir á **Hlaða niður skrá** til að hlaða niður gögnum sem flutt voru út frá þeirri einingu.</span><span class="sxs-lookup"><span data-stu-id="2afed-173">In the **Entity processing status** section, select the **Inventory value** entity in the list, and then select **Download file** to download the data that was exported from that entity.</span></span>

<span data-ttu-id="2afed-174">Nánari upplýsingar um hvernig á að nota gagnastjórnun til að flytja út gögn er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="2afed-174">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>