---
title: "Stuðningur við Kanban-flutningsbretti fyrir strikamerkjaskanna"
description: "Flutningstafla kanbans styður skönnun frá smátóls (widget) strikamerkjaskanna til að Velja, Hefja, Ljúka og Tæma kanban-vinnslu."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 29ad077cd10b0fa5967d145740f63051b05ad009
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="c36b3-103">Stuðningur við Kanban-flutningsbretti fyrir strikamerkjaskanna</span><span class="sxs-lookup"><span data-stu-id="c36b3-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c36b3-104">Flutningstafla kanbans styður skönnun frá smátóls (widget) strikamerkjaskanna til að Velja, Hefja, Ljúka og Tæma kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="c36b3-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="c36b3-105">Skráningarhamar</span><span class="sxs-lookup"><span data-stu-id="c36b3-105">Registration modes</span></span>
------------------

<span data-ttu-id="c36b3-106">Á **skráning Skanna** flýtiflipa er hægt að velja skráningarham sem stýrir aðgerðinni þegar kanban-spjaldnúmer er skannað eða númerið slegið handvirkt inn í númerareit kanban-spjalds.</span><span class="sxs-lookup"><span data-stu-id="c36b3-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="c36b3-107">Stilla skráningarham</span><span class="sxs-lookup"><span data-stu-id="c36b3-107">Set registration mode</span></span> | <span data-ttu-id="c36b3-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="c36b3-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c36b3-109">Hefja</span><span class="sxs-lookup"><span data-stu-id="c36b3-109">Start</span></span>                 | <span data-ttu-id="c36b3-110">Skrá flutningsvinnslu kanbans sem í vinnslu</span><span class="sxs-lookup"><span data-stu-id="c36b3-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="c36b3-111">Frágengið</span><span class="sxs-lookup"><span data-stu-id="c36b3-111">Complete</span></span>              | <span data-ttu-id="c36b3-112">Skrá flutningsvinnslu kanbans sem lokið</span><span class="sxs-lookup"><span data-stu-id="c36b3-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="c36b3-113">Autt</span><span class="sxs-lookup"><span data-stu-id="c36b3-113">Empty</span></span>                 | <span data-ttu-id="c36b3-114">Skráir efnismeðhöndlunareininguna sem kanban-kort vísar í sem tóma</span><span class="sxs-lookup"><span data-stu-id="c36b3-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="c36b3-115">Velja</span><span class="sxs-lookup"><span data-stu-id="c36b3-115">Select</span></span>                | <span data-ttu-id="c36b3-116">Skráir númer kanban-spjalds og velja vinnsluna sem vísað var í sjálfkrafa í kanban-lista</span><span class="sxs-lookup"><span data-stu-id="c36b3-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="c36b3-117">Velja skráningarham</span><span class="sxs-lookup"><span data-stu-id="c36b3-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="c36b3-118">Þegar notaður er strikamerkjaalesari til að velja vinnslu, breytist birtingarhamur kanban-spjalds.</span><span class="sxs-lookup"><span data-stu-id="c36b3-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="c36b3-119">Í þessari stillingu gilda eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="c36b3-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="c36b3-120">Aðeins skannaðs kanban-vinnslu birtist.</span><span class="sxs-lookup"><span data-stu-id="c36b3-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="c36b3-121">Upplýsingar um valið verk eru birtar í **upplýsingar** flýtiflipanum.</span><span class="sxs-lookup"><span data-stu-id="c36b3-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="c36b3-122">**Skilaboð** flýtiflipi birtir skilaboð aðeins fyrir valda vinnslu.</span><span class="sxs-lookup"><span data-stu-id="c36b3-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="c36b3-123">Hægt er að breyta stöðu vinnslunnar með því að nota eiginleika sem eru tiltækir í Aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="c36b3-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="c36b3-124">Flutningstafla Kanbans heldur áfram til að birta aðeins einni vinnslu við þessa tíma.</span><span class="sxs-lookup"><span data-stu-id="c36b3-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="c36b3-125">Hægt er að uppfæra upplýsingar í lista yfir vinnslur handvirkt með því að smella **Endurnýja** (Shift + F5) á við Aðgerðasvæði.</span><span class="sxs-lookup"><span data-stu-id="c36b3-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="c36b3-126">Eftir að þú endurnýjar upplýsingarnar birtast fullar niðurstöður fyrir síu vinnslu aftur.</span><span class="sxs-lookup"><span data-stu-id="c36b3-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="c36b3-127">Staða vinnslu og mögulegar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="c36b3-127">Job status and possible actions</span></span>
<span data-ttu-id="c36b3-128">Staða valinnar vinnslu og stöðuna á öllum föstum vinnslum fyrir tilvik kanbans, ákvarða hvort hægt sé að vinna vinnsluna frekar.</span><span class="sxs-lookup"><span data-stu-id="c36b3-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="c36b3-129">Eftirfarandi tafla birtir upplýsingar um þessar stöður og vinnslur:</span><span class="sxs-lookup"><span data-stu-id="c36b3-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="c36b3-130">Stöður sem eru tiltæk fyrir vinnslur eða efnismeðhöndlunareiningar sem er vísað í úr vinnslunum.</span><span class="sxs-lookup"><span data-stu-id="c36b3-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="c36b3-131">Hvert verk sem hægt er að framkvæma fyrir vinnslu.</span><span class="sxs-lookup"><span data-stu-id="c36b3-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c36b3-132">Vinnslugerð</span><span class="sxs-lookup"><span data-stu-id="c36b3-132">Job type</span></span></th>
<th><span data-ttu-id="c36b3-133">Staða Vinnslu eða staða efnismeðhöndlunareiningar</span><span class="sxs-lookup"><span data-stu-id="c36b3-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="c36b3-134">Uppfæra tiltektarlista</span><span class="sxs-lookup"><span data-stu-id="c36b3-134">Update picking list</span></span></th>
<th><span data-ttu-id="c36b3-135">Hefja</span><span class="sxs-lookup"><span data-stu-id="c36b3-135">Start</span></span></th>
<th><span data-ttu-id="c36b3-136">Uppfæra skráningu</span><span class="sxs-lookup"><span data-stu-id="c36b3-136">Update registration</span></span></th>
<th><span data-ttu-id="c36b3-137">Frágengið</span><span class="sxs-lookup"><span data-stu-id="c36b3-137">Complete</span></span></th>
<th><span data-ttu-id="c36b3-138">Autt</span><span class="sxs-lookup"><span data-stu-id="c36b3-138">Empty</span></span></th>
<th><span data-ttu-id="c36b3-139">Búa til tilvikskanban</span><span class="sxs-lookup"><span data-stu-id="c36b3-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c36b3-140">Flytja</span><span class="sxs-lookup"><span data-stu-id="c36b3-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="c36b3-141">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="c36b3-141">Not planned</span></span></li>
<li><span data-ttu-id="c36b3-142">Engin föst vinnsla eða fastar vinnslur eru loknar</span><span class="sxs-lookup"><span data-stu-id="c36b3-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="c36b3-143">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-143">Yes</span></span></td>
<td><span data-ttu-id="c36b3-144">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-144">Yes</span></span></td>
<td><span data-ttu-id="c36b3-145">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-145">Yes</span></span></td>
<td><span data-ttu-id="c36b3-146">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-146">Yes</span></span></td>
<td><span data-ttu-id="c36b3-147">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-147">No</span></span></td>
<td><span data-ttu-id="c36b3-148">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c36b3-149">Flytja</span><span class="sxs-lookup"><span data-stu-id="c36b3-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="c36b3-150">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="c36b3-150">Not planned</span></span></li>
<li><span data-ttu-id="c36b3-151">Föstu vinnslunni er ekki Lokið</span><span class="sxs-lookup"><span data-stu-id="c36b3-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="c36b3-152">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-152">Yes</span></span></td>
<td><span data-ttu-id="c36b3-153">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-153">No</span></span></td>
<td><span data-ttu-id="c36b3-154">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-154">Yes</span></span></td>
<td><span data-ttu-id="c36b3-155">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-155">No</span></span></td>
<td><span data-ttu-id="c36b3-156">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-156">No</span></span></td>
<td><span data-ttu-id="c36b3-157">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c36b3-158">Flytja</span><span class="sxs-lookup"><span data-stu-id="c36b3-158">Transfer</span></span></td>
<td><span data-ttu-id="c36b3-159">Í gangi</span><span class="sxs-lookup"><span data-stu-id="c36b3-159">In progress</span></span></td>
<td><span data-ttu-id="c36b3-160">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-160">Yes</span></span></td>
<td><span data-ttu-id="c36b3-161">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-161">No</span></span></td>
<td><span data-ttu-id="c36b3-162">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-162">Yes</span></span></td>
<td><span data-ttu-id="c36b3-163">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-163">Yes</span></span></td>
<td><span data-ttu-id="c36b3-164">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-164">No</span></span></td>
<td><span data-ttu-id="c36b3-165">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c36b3-166">Flytja</span><span class="sxs-lookup"><span data-stu-id="c36b3-166">Transfer</span></span></td>
<td><span data-ttu-id="c36b3-167">Lokið</span><span class="sxs-lookup"><span data-stu-id="c36b3-167">Completed</span></span></td>
<td><span data-ttu-id="c36b3-168">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-168">No</span></span></td>
<td><span data-ttu-id="c36b3-169">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-169">No</span></span></td>
<td><span data-ttu-id="c36b3-170">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-170">No</span></span></td>
<td><span data-ttu-id="c36b3-171">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-171">No</span></span></td>
<td><span data-ttu-id="c36b3-172">Já</span><span class="sxs-lookup"><span data-stu-id="c36b3-172">Yes</span></span></td>
<td><span data-ttu-id="c36b3-173">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c36b3-174">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="c36b3-174">Transfer or process</span></span></td>
<td><span data-ttu-id="c36b3-175">Autt</span><span class="sxs-lookup"><span data-stu-id="c36b3-175">Empty</span></span></td>
<td><span data-ttu-id="c36b3-176">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-176">No</span></span></td>
<td><span data-ttu-id="c36b3-177">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-177">No</span></span></td>
<td><span data-ttu-id="c36b3-178">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-178">No</span></span></td>
<td><span data-ttu-id="c36b3-179">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-179">No</span></span></td>
<td><span data-ttu-id="c36b3-180">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-180">No</span></span></td>
<td><span data-ttu-id="c36b3-181">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c36b3-182">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="c36b3-182">Transfer or process</span></span></td>
<td><span data-ttu-id="c36b3-183">Kanban-spjald finnst ekki</span><span class="sxs-lookup"><span data-stu-id="c36b3-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="c36b3-184">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-184">No</span></span></td>
<td><span data-ttu-id="c36b3-185">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-185">No</span></span></td>
<td><span data-ttu-id="c36b3-186">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-186">No</span></span></td>
<td><span data-ttu-id="c36b3-187">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-187">No</span></span></td>
<td><span data-ttu-id="c36b3-188">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-188">No</span></span></td>
<td><span data-ttu-id="c36b3-189">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c36b3-190">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="c36b3-190">Transfer or process</span></span></td>
<td><span data-ttu-id="c36b3-191">Kanban-spjald finnst, en það er ekki úthlutuð til kanban</span><span class="sxs-lookup"><span data-stu-id="c36b3-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="c36b3-192">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-192">No</span></span></td>
<td><span data-ttu-id="c36b3-193">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-193">No</span></span></td>
<td><span data-ttu-id="c36b3-194">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-194">No</span></span></td>
<td><span data-ttu-id="c36b3-195">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-195">No</span></span></td>
<td><span data-ttu-id="c36b3-196">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-196">No</span></span></td>
<td><span data-ttu-id="c36b3-197">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c36b3-198">Ferli</span><span class="sxs-lookup"><span data-stu-id="c36b3-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="c36b3-199">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="c36b3-199">Not planned</span></span></li>
<li><span data-ttu-id="c36b3-200">Undirbúið</span><span class="sxs-lookup"><span data-stu-id="c36b3-200">Prepared</span></span></li>
<li><span data-ttu-id="c36b3-201">Í gangi</span><span class="sxs-lookup"><span data-stu-id="c36b3-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="c36b3-202">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-202">No</span></span></td>
<td><span data-ttu-id="c36b3-203">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-203">No</span></span></td>
<td><span data-ttu-id="c36b3-204">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-204">No</span></span></td>
<td><span data-ttu-id="c36b3-205">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-205">No</span></span></td>
<td><span data-ttu-id="c36b3-206">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-206">No</span></span></td>
<td><span data-ttu-id="c36b3-207">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c36b3-208">Ferli</span><span class="sxs-lookup"><span data-stu-id="c36b3-208">Process</span></span></td>
<td><span data-ttu-id="c36b3-209">Lokið</span><span class="sxs-lookup"><span data-stu-id="c36b3-209">Completed</span></span></td>
<td><span data-ttu-id="c36b3-210">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-210">No</span></span></td>
<td><span data-ttu-id="c36b3-211">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-211">No</span></span></td>
<td><span data-ttu-id="c36b3-212">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-212">No</span></span></td>
<td><span data-ttu-id="c36b3-213">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-213">No</span></span></td>
<td><span data-ttu-id="c36b3-214">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-214">No</span></span></td>
<td><span data-ttu-id="c36b3-215">Nei</span><span class="sxs-lookup"><span data-stu-id="c36b3-215">No</span></span></td>
</tr>
</tbody>
</table>






