---
title: Fylgjast með keyrslu áætlanagerðar
description: Þetta efni útskýrir hvernig framleiðslustjóri getur séð hvort keyrsla aðaláætlunargerðar er í gangi.
author: josaw1
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1733562768b3fe869f326bbfb47b6135a91b5cb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829643"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="aa1d2-103">Fylgjast með keyrslu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="aa1d2-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="aa1d2-104">Notaðu Gantt myndrit til að sjá framvindu aðaláætlunargerðar</span><span class="sxs-lookup"><span data-stu-id="aa1d2-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="aa1d2-105">Af síðunni **Skoða framvindu aðaláætlunargerðar** geturðu skoðað upplýsingar um sögulegar keyrslur aðaláætlunargerðar sem Gantt kort.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="aa1d2-106">Þessi virkni getur hjálpað þér að skilja tímann sem er eytt í hina ýmsu áfanga aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="aa1d2-107">Fyrir núverandi virkt skipulagsstarf er hægt að nota síðuna **Skoða framvindu aðaláætlunargerðar** til að fylgjast með framvindu mála og skoða þann áætlaða tíma sem eftir er.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="aa1d2-108">Kveiktu á og notaðu eiginleikann Framvindubirting aðaláætlunargerðar</span><span class="sxs-lookup"><span data-stu-id="aa1d2-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="aa1d2-109">Til að nota þessa virkni skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="aa1d2-110">Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Nýtt**, velurðu **Framvindubirting aðaláætlunargerðar** á listanum.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="aa1d2-111">Ef eiginleikinn birtist ekki á flipanum **Nýtt** skaltu líta á flipana **Ekki gert virkt** og **Allt**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="aa1d2-112">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-112">Select **Enable now**.</span></span> <span data-ttu-id="aa1d2-113">Að öðrum kosti velurðu **Áætlun** og velur síðan tímann þegar kveikt skal á aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="aa1d2-114">Síðan **Skoða framvindu aðaláætlunargerðar** getur sýnt bæði sögulegar vinnslur áætlunargerðar og virkar vinnslur áætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="aa1d2-115">Það eru tveir möguleikar til að skoða sögulegar áætlunarvinnslur.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="aa1d2-116">Farðu í **Aðaláætlunargerð \> Uppsetning \> Áætlanir \> Aðaláætlanir** og veldu síðan á aðgerðarrúðunni **Saga**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="aa1d2-117">Veldu þá vinnslu sem þú vilt velja, veldu **Fyrirspurnir** og veldu síðan **Skoða framvindu**</span><span class="sxs-lookup"><span data-stu-id="aa1d2-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="aa1d2-118">Farðu í **Aðaláætlanagerð \> Vinnusvæði \> Aðaláætlunargerð**, í aðaláætlunargerðarreitnum smellirðu á **Saga**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="aa1d2-119">Veldu þá vinnslu sem þú vilt velja, veldu **Fyrirspurnir** og veldu síðan **Skoða framvindu**</span><span class="sxs-lookup"><span data-stu-id="aa1d2-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="aa1d2-120">Það eru tveir möguleikar til að skoða virkar áætlunarvinnslur.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="aa1d2-121">Farðu í **Aðaláætlunargerð \> Vinnusvæði \> Aðaláætlunargerð**, veldu á aðgerðarglugganum **Óunnið áætlunarferli**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="aa1d2-122">Veldu þá vinnslu sem þú vilt velja, veldu **Fyrirspurnir** og veldu síðan **Skoða framvindu**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="aa1d2-123">Farðu í **Aðaláætlanagerð \> Vinnusvæði \> Aðaláætlunargerð**, í aðaláætlunargerðarreitnum smellirðu á **Skoða framvindu**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="aa1d2-124">Veldu þá vinnslu sem þú vilt velja, veldu **Fyrirspurnir** og veldu síðan **Skoða framvindu**</span><span class="sxs-lookup"><span data-stu-id="aa1d2-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="aa1d2-125">Athugaðu að þú getur aðeins skoðað virk störf þegar áætlunargerðarvinnsla er í gangi.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="aa1d2-126">Greindu vinnslu aðaláætlunargerðar</span><span class="sxs-lookup"><span data-stu-id="aa1d2-126">Analyze a master planning job</span></span>

<span data-ttu-id="aa1d2-127">Í Gantt töflunni geturðu stækkað sérhvert eftirfarandi skipulagsferla til að skoða frekari upplýsingar um tímann sem er varið:</span><span class="sxs-lookup"><span data-stu-id="aa1d2-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="aa1d2-128">Frumstilling</span><span class="sxs-lookup"><span data-stu-id="aa1d2-128">Initializing</span></span>
- <span data-ttu-id="aa1d2-129">Gögnum eytt og bætt við</span><span class="sxs-lookup"><span data-stu-id="aa1d2-129">Deleting and inserting data</span></span>
- <span data-ttu-id="aa1d2-130">Þekjuáætlun</span><span class="sxs-lookup"><span data-stu-id="aa1d2-130">Coverage planning</span></span>
- <span data-ttu-id="aa1d2-131">Seinkanir</span><span class="sxs-lookup"><span data-stu-id="aa1d2-131">Delays</span></span>
- <span data-ttu-id="aa1d2-132">Aðgerðaboð</span><span class="sxs-lookup"><span data-stu-id="aa1d2-132">Action messages</span></span>
- <span data-ttu-id="aa1d2-133">Lok</span><span class="sxs-lookup"><span data-stu-id="aa1d2-133">Finalization</span></span>
- <span data-ttu-id="aa1d2-134">Sjálfvirk staðfesting</span><span class="sxs-lookup"><span data-stu-id="aa1d2-134">Auto-firming</span></span>

<span data-ttu-id="aa1d2-135">Gantt taflan er gagnlegt tól ef þú vilt skoða áhrifin af því að nota aðgerðarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="aa1d2-136">Leiðsögn í Gantt töflunni</span><span class="sxs-lookup"><span data-stu-id="aa1d2-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="aa1d2-137">Til að stækka valinn hóp og sýna smáatriðin, veldu plúsmerki (**+**) í trjásýninni.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="aa1d2-138">Til að fella hópinn sem valinn er saman skaltu velja mínustáknið (**-**) í trjásýninni.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="aa1d2-139">Þú getur notað lyklaborðið þitt til að fletta.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="aa1d2-140">Notaðu takkana **Upp-ör** og **Niður-ör** til að fara á milli lína.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="aa1d2-141">Notaðu takkana **Hægri-ör** og **Vinstri-ör** til að stækka og fella saman hópa.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="aa1d2-142">Til að opna eða loka öllum stigum í Gantt töflunni velurðu **Stækka allt** eða **Fella allt saman**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="aa1d2-143">Til að skoða tengdan vinnslutíma heldurðu músarbendlinum yfir verki.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="aa1d2-144">(Verk eru lægsta stigið í Gantt töflunni.)</span><span class="sxs-lookup"><span data-stu-id="aa1d2-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="aa1d2-145">Skoða viðbótarkeyrslu aðaláætlunargerðar til að bera saman störf</span><span class="sxs-lookup"><span data-stu-id="aa1d2-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="aa1d2-146">Með því að velja vinnslu aðaláætlunargerðar í reitnum **Sýna viðbótarkeyrslu aðaláætlunargerðar** geturðu skoðað viðbótarkeyrslu aðaláætlunargerðar í Gantt töflunni og borið saman vinnslurnar tvær.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="aa1d2-147">BOM-stig skjár</span><span class="sxs-lookup"><span data-stu-id="aa1d2-147">BOM-level display</span></span>

<span data-ttu-id="aa1d2-148">Uppskriftarstig (BOM) eru sýnd á annan hátt vegna þekjuáætlanagerðar, tafa, aðgerða og styrkingar.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="aa1d2-149">**Þekjuáætlanagerð** - BOM-stig eru sýnd eins og búist var við.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="aa1d2-150">Þau eru reiknuð frá toppi og niður.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="aa1d2-151">**Dæmi:** BOM stig 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="aa1d2-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="aa1d2-152">**Tafir** - BOM stig eru sýnd sem umfang áætlunar BOM margfaldað með –1.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="aa1d2-153">(Með öðrum orðum, þau hafa neikvætt merki.)</span><span class="sxs-lookup"><span data-stu-id="aa1d2-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="aa1d2-154">**Dæmi:** BOM stig –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="aa1d2-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="aa1d2-155">**Aðgerðaskilaboð** - BOM-stig eru sýnd eins og búist var við.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="aa1d2-156">Þau eru reiknuð frá toppi og niður.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="aa1d2-157">**Dæmi:** BOM stig 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="aa1d2-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="aa1d2-158">**Sjálfvirk styrking** - BOM stig eru sýnd sem 999 að frádregnu BOM-stigi þekjuáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="aa1d2-159">**Dæmi:** BOM stig 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="aa1d2-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="aa1d2-160">Eftirfarandi tafla dregur saman hegðunina.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="aa1d2-161">BOM stig sem er sýnt</span><span class="sxs-lookup"><span data-stu-id="aa1d2-161">BOM level that is shown</span></span> | <span data-ttu-id="aa1d2-162">Endanleg vara</span><span class="sxs-lookup"><span data-stu-id="aa1d2-162">End item</span></span> | <span data-ttu-id="aa1d2-163">Undiríhlutur</span><span class="sxs-lookup"><span data-stu-id="aa1d2-163">Subcomponent</span></span> | <span data-ttu-id="aa1d2-164">Hráefni</span><span class="sxs-lookup"><span data-stu-id="aa1d2-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="aa1d2-165">Þekjuáætlun</span><span class="sxs-lookup"><span data-stu-id="aa1d2-165">Coverage planning</span></span> | <span data-ttu-id="aa1d2-166">0</span><span class="sxs-lookup"><span data-stu-id="aa1d2-166">0</span></span> | <span data-ttu-id="aa1d2-167">1</span><span class="sxs-lookup"><span data-stu-id="aa1d2-167">1</span></span> | <span data-ttu-id="aa1d2-168">2</span><span class="sxs-lookup"><span data-stu-id="aa1d2-168">2</span></span> |
| <span data-ttu-id="aa1d2-169">Seinkanir</span><span class="sxs-lookup"><span data-stu-id="aa1d2-169">Delays</span></span> | <span data-ttu-id="aa1d2-170">0</span><span class="sxs-lookup"><span data-stu-id="aa1d2-170">0</span></span> | <span data-ttu-id="aa1d2-171">–1</span><span class="sxs-lookup"><span data-stu-id="aa1d2-171">–1</span></span> | <span data-ttu-id="aa1d2-172">–2</span><span class="sxs-lookup"><span data-stu-id="aa1d2-172">–2</span></span> |
| <span data-ttu-id="aa1d2-173">Aðgerðaboð</span><span class="sxs-lookup"><span data-stu-id="aa1d2-173">Action message</span></span> | <span data-ttu-id="aa1d2-174">0</span><span class="sxs-lookup"><span data-stu-id="aa1d2-174">0</span></span> | <span data-ttu-id="aa1d2-175">1</span><span class="sxs-lookup"><span data-stu-id="aa1d2-175">1</span></span> | <span data-ttu-id="aa1d2-176">2</span><span class="sxs-lookup"><span data-stu-id="aa1d2-176">2</span></span> |
| <span data-ttu-id="aa1d2-177">Sjálfvirk staðfesting</span><span class="sxs-lookup"><span data-stu-id="aa1d2-177">Auto-firming</span></span> | <span data-ttu-id="aa1d2-178">999</span><span class="sxs-lookup"><span data-stu-id="aa1d2-178">999</span></span> | <span data-ttu-id="aa1d2-179">998</span><span class="sxs-lookup"><span data-stu-id="aa1d2-179">998</span></span> | <span data-ttu-id="aa1d2-180">997</span><span class="sxs-lookup"><span data-stu-id="aa1d2-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="aa1d2-181">Gera framvindu sýnilega</span><span class="sxs-lookup"><span data-stu-id="aa1d2-181">Visualize progress</span></span>

<span data-ttu-id="aa1d2-182">Ef þú skoðar vinnslu aðaláætlunargerðar sem er í gangi er framvinda sýnd með litum í Gantt töflunni.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="aa1d2-183">Eftirfarandi litir eiga við um bláa þemað.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="aa1d2-184">Fyrir önnur litaþemu eru litirnir aðrir.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="aa1d2-185">**Dökkblátt** - Lokin áætlunarverk.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="aa1d2-186">**Appelsínugult** - Verkið sem nú er í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="aa1d2-187">**Ljósblátt** - Mat á verkum sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="aa1d2-188">Liturinn er aðeins sýndur á lægsta stiginu í Gantt töflunni.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="aa1d2-189">Veldu **Auka allt** að skoða öll verk í vinnslu aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="aa1d2-190">Mat á verkum sem eftir eru byggist á sögulegum vinnslu aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="aa1d2-191">Keyra aðaláætlunargerð og fylgjast með vinnslutíma</span><span class="sxs-lookup"><span data-stu-id="aa1d2-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="aa1d2-192">Veldu á sjálfgefna mælaborðinu **Aðaláætlunargerð**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="aa1d2-193">Í reitinn **Áætlun** slærðu inn eða velur gildi.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="aa1d2-194">Veljið **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-194">Select **Run**.</span></span>
1. <span data-ttu-id="aa1d2-195">Stilltu valkostinn **Rekja vinnslutíma** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="aa1d2-196">Í reitinn **Fjöldi þráða** skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="aa1d2-197">Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="aa1d2-198">Veldu línuna þar sem reiturinn **Reitur** er stilltur á **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="aa1d2-199">Í reitinn **Skilyrði** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="aa1d2-200">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="aa1d2-200">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]