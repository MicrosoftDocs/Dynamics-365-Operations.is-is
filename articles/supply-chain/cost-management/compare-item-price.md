---
title: Berðu saman geymsluskýrslu vöruverðs
description: Lærðu hvernig á að búa til samanburðarskýrslu um vöruverð og fletta síðan og/eða flytja út niðurstöðuna.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 73e43a685f390fd718028de6add0370dfcd6cf3b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430533"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="6d73c-103">Berðu saman geymsluskýrslu vöruverðs</span><span class="sxs-lookup"><span data-stu-id="6d73c-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d73c-104">Þetta efni útskýrir hvernig á að keyra skýrsluna **Bera saman geymslu vöruverðs** og gerir úttakið tiltækt á stafrænu formi, annaðhvort sem gagnvirka síðu í Dynamics 365 Supply Chain Management, eða sem útflutt skjal á einhverju af nokkrum sniðum.</span><span class="sxs-lookup"><span data-stu-id="6d73c-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="6d73c-105">Þegar þú skoðar skýrsluna í vafranum er dálkum og samanlögðum stöðum gagnvirkt breytt, allt eftir stilltu skipulagi.</span><span class="sxs-lookup"><span data-stu-id="6d73c-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="6d73c-106">Þú getur flokkað niðurstöðurnar, síað þær, borað niður í gögnin og fleira.</span><span class="sxs-lookup"><span data-stu-id="6d73c-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="6d73c-107">Niðurstöður skýrslunnar eru vistaðar í gagnaeiningunni **Bera saman vöruverð**, sem gerir þér kleift að sía og flytja niðurstöðurnar á snið eins og CSV eða Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6d73c-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="6d73c-108">Skýrslan **Bera saman vöruverðsgeymslu** er gagnleg í tilfellum þar sem úttakið inniheldur margar línur.</span><span class="sxs-lookup"><span data-stu-id="6d73c-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="6d73c-109">Til dæmis mun framleiðsla innihalda margar línur ef þú ert með meira en 40.000 hluti sem eru með verð á vöru í bið í útgáfu kostnaðarútreiknings.</span><span class="sxs-lookup"><span data-stu-id="6d73c-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="6d73c-110">Virkja samanburð á geymsluskýrslu vöruverðs</span><span class="sxs-lookup"><span data-stu-id="6d73c-110">Enable compare item prices storage</span></span>

<span data-ttu-id="6d73c-111">Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="6d73c-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="6d73c-112">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleika og virkja hann ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="6d73c-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="6d73c-113">Hérna er eiginleikinn skráður sem:</span><span class="sxs-lookup"><span data-stu-id="6d73c-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="6d73c-114">**Eining** - Kostnaðarstjórnun</span><span class="sxs-lookup"><span data-stu-id="6d73c-114">**Module** - Cost management</span></span>
- <span data-ttu-id="6d73c-115">**Heiti eiginleika** - Bera saman geymslu vöruverðs</span><span class="sxs-lookup"><span data-stu-id="6d73c-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="6d73c-116">Búa til skýrsluna Bera saman vöruverðsgeymslu</span><span class="sxs-lookup"><span data-stu-id="6d73c-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="6d73c-117">Fylgdu þessum skrefum til að búa til og geyma skýrsluna **Bera saman geymslu vöruverðs**:</span><span class="sxs-lookup"><span data-stu-id="6d73c-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="6d73c-118">Farðu í **Kostnaðarstjórnun > Fyrirspurnir og skýrslur > Fyrirframákveðnar kostnaðarskýrslur > Bera saman geymslu vöruverðs**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="6d73c-119">Veldu **Nýtt** til að opna gluggann **Bera saman vöruverð**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="6d73c-120">Stilltu eftirfarandi valkosti til að skilgreina hvaða verð á að bera saman í skýrslunni:</span><span class="sxs-lookup"><span data-stu-id="6d73c-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="6d73c-121">Á flýtiflipanum **Færibreytur** gefurðu skýrslunni einkvæmt **Heiti** og notar reitina í hlutunum **Verð bíður samanburðar** og **Verð notað til samanburðar** til að skilgreina hvaða verð og dagsetningar á að bera saman.</span><span class="sxs-lookup"><span data-stu-id="6d73c-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="6d73c-122">Á flýtiflipanum **Færslur til að taka með** seturðu upp síur og skorður til að skilgreina hvaða gögn skýrslan á að innihalda.</span><span class="sxs-lookup"><span data-stu-id="6d73c-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="6d73c-123">Á flýtiflipanum **Keyra í bakgrunni** seturðu upp hvernig, hvenær og hversu oft þú vilt búa til skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="6d73c-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="6d73c-124">Þessi skýrsla er alltaf framkvæmd sem hluti af runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="6d73c-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="6d73c-125">Veldu **Í lagi** til að beita stillingum þínum og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="6d73c-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="6d73c-126">Eftir að runuvinnslunni er lokið verður hún skráð á síðunni **Bera saman geymslu vöruverðs**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="6d73c-127">Það gæti þurft að endurræsa síðuna til að sjá skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="6d73c-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="6d73c-128">Skoðaðu skýrsluna Bera saman vöruverðsgeymslu</span><span class="sxs-lookup"><span data-stu-id="6d73c-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="6d73c-129">Eftir að þú hefur búið til skýrslu geturðu skoðað og kannað hana hvenær sem er á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="6d73c-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="6d73c-130">Farðu í **Kostnaðarstjórnun > Fyrirspurnir og skýrslur > Fyrirframákveðnar kostnaðarskýrslur > Bera saman geymslu vöruverðs**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="6d73c-131">Velja skýrslu af listanum.</span><span class="sxs-lookup"><span data-stu-id="6d73c-131">Select a report from the list.</span></span>

1. <span data-ttu-id="6d73c-132">Gerið eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="6d73c-132">Do one of the following:</span></span>

    - <span data-ttu-id="6d73c-133">Veldu **Yfirlit** til að fá yfirsýn yfir niðurstöður skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="6d73c-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="6d73c-134">Veldu **Skoða upplýsingar** til að fá nánari yfirsýn yfir skýrsluna þína</span><span class="sxs-lookup"><span data-stu-id="6d73c-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="6d73c-135">Eftir að valið yfirlit opnast er hægt að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="6d73c-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="6d73c-136">Veldu næstum hvaða dálkafyrirsögn sem er til að flokka eða sía töfluna eftir gildum í þeim dálki, rétt eins og á flestum stöðluðum eyðublöðum í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6d73c-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="6d73c-137">Athugaðu að þú getur ekki flokkað eða síað dálkinn **Nettóbreyting verðs %** þar sem að það er reiknaður reitur.</span><span class="sxs-lookup"><span data-stu-id="6d73c-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="6d73c-138">Veldu **Birting vídda** til að opna glugga þar sem þú getur valið hvaða víddardálk á að hafa með í forminu.</span><span class="sxs-lookup"><span data-stu-id="6d73c-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="6d73c-139">Stilltu **Vista skipulag** á **Já** ef þú vilt vista þessar stillingar svo þær verði varðveittar næst þegar þú opnar skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="6d73c-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="6d73c-140">Veldu **Í lagi** til að beita stillingum þínum og loka.</span><span class="sxs-lookup"><span data-stu-id="6d73c-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="6d73c-141">Veldu einhverja röð á forminu og veldu síðan **Skoða upplýsingar** til að sjá frekari upplýsingar um valda vöru.</span><span class="sxs-lookup"><span data-stu-id="6d73c-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="6d73c-142">Þú getur borið niður í gögn héðan.</span><span class="sxs-lookup"><span data-stu-id="6d73c-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="6d73c-143">Veldu einhverja röð á forminu og veldu síðan **Skoða samanburðartöflu** til að sjá gagnvirka myndræna framsetningu á niðurstöðum þínum þegar þær tengjast vörunni sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="6d73c-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="6d73c-144">Þú getur kannað þessar niðurstöður með því að velja ýmsa myndræna þætti í töflunni og skýringartextanum.</span><span class="sxs-lookup"><span data-stu-id="6d73c-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="6d73c-145">Veldu einhverja röð á forminu og veldu síðan **Skoða útreikningsupplýsingar** til að sjá frekari upplýsingar um útreikninga á valinni vöru.</span><span class="sxs-lookup"><span data-stu-id="6d73c-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="6d73c-146">Þú getur borið niður í gögn héðan.</span><span class="sxs-lookup"><span data-stu-id="6d73c-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="6d73c-147">Flyttu út skýrsluna Bera saman vöruverðsgeymslu</span><span class="sxs-lookup"><span data-stu-id="6d73c-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="6d73c-148">Sérhver skýrsla sem þú býrð til er vistuð í gagnaeiningunni **Bera saman vöruverð**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="6d73c-149">Þú getur notað staðlaða gagnastjórnunareiginleika Supply Chain Management til að flytja gögn út úr þessari einingu á hvaða studda gagnasnið sem er, þar á meðal CSV eða Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6d73c-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="6d73c-150">Eftirfarandi er dæmi um hvernig á að flytja út skýrsluna **Bera saman geymslu vöruverðs**:</span><span class="sxs-lookup"><span data-stu-id="6d73c-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="6d73c-151">Farðu í **Kerfisstjórnun > Vinnusvæði > Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="6d73c-152">Veldu hnappinn **Flytja út** í hlutanum **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="6d73c-153">Síðan **Fltyja út** opnast, sem þú notar til að setja upp útflutningsvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="6d73c-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="6d73c-154">Byrjaðu á því að gefa vinnslunni **Heiti hóps**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="6d73c-155">Í hlutanum **Valdar einingar** velurðu **Bæta við einingu** til að opna valmynd þar sem þú getur stillt eftirfarandi valkosti:</span><span class="sxs-lookup"><span data-stu-id="6d73c-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="6d73c-156">**Heiti einingar** - Veldu **Bera saman vöruverð**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="6d73c-157">**Markgagnasnið** - Veldu sniðið sem þú vilt flytja út á.</span><span class="sxs-lookup"><span data-stu-id="6d73c-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="6d73c-158">Veldu **Bæta við** til að bæta við nýju röðinni og veldu síðan **Loka** til að loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="6d73c-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="6d73c-159">Venjulega flyturðu út eina skýrslu í einu.</span><span class="sxs-lookup"><span data-stu-id="6d73c-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="6d73c-160">Til að gera þetta seturðu upp **Síu** fyrir röðina sem þú varst að bæta við glugganum **Fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="6d73c-161">Þetta gerir þér kleift að skilgreina hvaða skýrslur úr einingunni **Bera saman vöruverð** sem þú vilt hafa með í útflutningi þínum.</span><span class="sxs-lookup"><span data-stu-id="6d73c-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="6d73c-162">Stilltu eftirfarandi síuvalkosti til að flytja út staka skýrslu:</span><span class="sxs-lookup"><span data-stu-id="6d73c-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="6d73c-163">Á flipanum **Svið** velurðu **Bæta við** til að bæta við nýrri röð.</span><span class="sxs-lookup"><span data-stu-id="6d73c-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="6d73c-164">Stilltu **Töflu** á **Bera saman vöruverð**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="6d73c-165">Stilltu **Afleidda töflu** á **Bera saman vöruverð**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="6d73c-166">Stilltu **Reit** á reitinn sem þú vilt sía eftir.</span><span class="sxs-lookup"><span data-stu-id="6d73c-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="6d73c-167">Venjulega munt þú nota **Heiti framkvæmdar** eða **Framkvæmdartími**.</span><span class="sxs-lookup"><span data-stu-id="6d73c-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="6d73c-168">Stilltu **Viðmið** á gildið úr völdum reit sem þú vilt leita að (annaðhvort heiti skýrslunnar eða tíminn sem skýrslan var búin til).</span><span class="sxs-lookup"><span data-stu-id="6d73c-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="6d73c-169">Bætið við fleiri línum við töfluna **Svið** töflu þar til þú hefur bent á skýrsluna sem þú ert að leita að á einstakan hátt.</span><span class="sxs-lookup"><span data-stu-id="6d73c-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="6d73c-170">Veldu **Í lagi** til að vista stillingarnar og loka.</span><span class="sxs-lookup"><span data-stu-id="6d73c-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="6d73c-171">Veldu **Vista** til að vista uppsetningu á útflutningi.</span><span class="sxs-lookup"><span data-stu-id="6d73c-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="6d73c-172">Opnaðu flipann **Valkostir útflutnings** og veldu **Flytja út núna** til að búa til útflutningsskrána.</span><span class="sxs-lookup"><span data-stu-id="6d73c-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="6d73c-173">Síðan **Yfirlit framkvæmdar** opnast þar sem þú getur séð stöðuna á útflutningsvinnslunni og lista yfir þær einingar sem voru fluttar út.</span><span class="sxs-lookup"><span data-stu-id="6d73c-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="6d73c-174">Veldu eininguna **Bera saman vöruverð** sem er skráð í reitinn **Vinnslustaða einingar** og veldu síðan **Sækja skrá** til að sækja gögnin sem flutt eru út úr þeirri einingu.</span><span class="sxs-lookup"><span data-stu-id="6d73c-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="6d73c-175">Nánari upplýsingar um hvernig á að nota gagnastjórnun til að flytja út gögn er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="6d73c-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
