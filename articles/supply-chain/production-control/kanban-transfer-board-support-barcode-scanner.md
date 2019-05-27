---
title: Stuðningur við Kanban-flutningsbretti fyrir strikamerkjaskanna
description: Flutningstafla kanbans styður skönnun frá smátóls (widget) strikamerkjaskanna til að Velja, Hefja, Ljúka og Tæma kanban-vinnslu.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63a33af63144b78d0c375022b9802e11c255598
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569218"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="e37f9-103">Stuðningur við Kanban-flutningsbretti fyrir strikamerkjaskanna</span><span class="sxs-lookup"><span data-stu-id="e37f9-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e37f9-104">Flutningstafla kanbans styður skönnun frá smátóls (widget) strikamerkjaskanna til að Velja, Hefja, Ljúka og Tæma kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="e37f9-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="e37f9-105">Skráningarhamar</span><span class="sxs-lookup"><span data-stu-id="e37f9-105">Registration modes</span></span>
------------------

<span data-ttu-id="e37f9-106">Á **skráning Skanna** flýtiflipa er hægt að velja skráningarham sem stýrir aðgerðinni þegar kanban-spjaldnúmer er skannað eða númerið slegið handvirkt inn í númerareit kanban-spjalds.</span><span class="sxs-lookup"><span data-stu-id="e37f9-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="e37f9-107">Stilla skráningarham</span><span class="sxs-lookup"><span data-stu-id="e37f9-107">Set registration mode</span></span> | <span data-ttu-id="e37f9-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e37f9-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e37f9-109">Hefja</span><span class="sxs-lookup"><span data-stu-id="e37f9-109">Start</span></span>                 | <span data-ttu-id="e37f9-110">Skrá flutningsvinnslu kanbans sem í vinnslu</span><span class="sxs-lookup"><span data-stu-id="e37f9-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="e37f9-111">Frágengið</span><span class="sxs-lookup"><span data-stu-id="e37f9-111">Complete</span></span>              | <span data-ttu-id="e37f9-112">Skrá flutningsvinnslu kanbans sem lokið</span><span class="sxs-lookup"><span data-stu-id="e37f9-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="e37f9-113">Autt</span><span class="sxs-lookup"><span data-stu-id="e37f9-113">Empty</span></span>                 | <span data-ttu-id="e37f9-114">Skráir efnismeðhöndlunareininguna sem kanban-kort vísar í sem tóma</span><span class="sxs-lookup"><span data-stu-id="e37f9-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="e37f9-115">Velja</span><span class="sxs-lookup"><span data-stu-id="e37f9-115">Select</span></span>                | <span data-ttu-id="e37f9-116">Skráir númer kanban-spjalds og velja vinnsluna sem vísað var í sjálfkrafa í kanban-lista</span><span class="sxs-lookup"><span data-stu-id="e37f9-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="e37f9-117">Velja skráningarham</span><span class="sxs-lookup"><span data-stu-id="e37f9-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="e37f9-118">Þegar notaður er strikamerkjaalesari til að velja vinnslu, breytist birtingarhamur kanban-spjalds.</span><span class="sxs-lookup"><span data-stu-id="e37f9-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="e37f9-119"> Í þessari stillingu gilda eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="e37f9-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="e37f9-120">Aðeins skannaðs kanban-vinnslu birtist.</span><span class="sxs-lookup"><span data-stu-id="e37f9-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="e37f9-121">Upplýsingar um valið verk eru birtar í **upplýsingar** flýtiflipanum.</span><span class="sxs-lookup"><span data-stu-id="e37f9-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="e37f9-122">**Skilaboð** flýtiflipi birtir skilaboð aðeins fyrir valda vinnslu.</span><span class="sxs-lookup"><span data-stu-id="e37f9-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="e37f9-123">Hægt er að breyta stöðu vinnslunnar með því að nota eiginleika sem eru tiltækir í Aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="e37f9-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="e37f9-124">Flutningstafla Kanbans heldur áfram til að birta aðeins einni vinnslu við þessa tíma.</span><span class="sxs-lookup"><span data-stu-id="e37f9-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="e37f9-125">Hægt er að uppfæra upplýsingar í lista yfir vinnslur handvirkt með því að smella **Endurnýja** (Shift + F5) á við Aðgerðasvæði.</span><span class="sxs-lookup"><span data-stu-id="e37f9-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="e37f9-126">Eftir að þú endurnýjar upplýsingarnar birtast fullar niðurstöður fyrir síu vinnslu aftur.</span><span class="sxs-lookup"><span data-stu-id="e37f9-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="e37f9-127">Staða vinnslu og mögulegar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="e37f9-127">Job status and possible actions</span></span>
<span data-ttu-id="e37f9-128">Staða valinnar vinnslu og stöðuna á öllum föstum vinnslum fyrir tilvik kanbans, ákvarða hvort hægt sé að vinna vinnsluna frekar.</span><span class="sxs-lookup"><span data-stu-id="e37f9-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="e37f9-129">Eftirfarandi tafla birtir upplýsingar um þessar stöður og vinnslur:</span><span class="sxs-lookup"><span data-stu-id="e37f9-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="e37f9-130">Stöður sem eru tiltæk fyrir vinnslur eða efnismeðhöndlunareiningar sem er vísað í úr vinnslunum.</span><span class="sxs-lookup"><span data-stu-id="e37f9-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="e37f9-131">Hvert verk sem hægt er að framkvæma fyrir vinnslu.</span><span class="sxs-lookup"><span data-stu-id="e37f9-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="e37f9-132">Vinnslugerð</span><span class="sxs-lookup"><span data-stu-id="e37f9-132">Job type</span></span></th>
<th><span data-ttu-id="e37f9-133">Staða Vinnslu eða staða efnismeðhöndlunareiningar</span><span class="sxs-lookup"><span data-stu-id="e37f9-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="e37f9-134">Uppfæra tiltektarlista</span><span class="sxs-lookup"><span data-stu-id="e37f9-134">Update picking list</span></span></th>
<th><span data-ttu-id="e37f9-135">Hefja</span><span class="sxs-lookup"><span data-stu-id="e37f9-135">Start</span></span></th>
<th><span data-ttu-id="e37f9-136">Uppfæra skráningu</span><span class="sxs-lookup"><span data-stu-id="e37f9-136">Update registration</span></span></th>
<th><span data-ttu-id="e37f9-137">Frágengið</span><span class="sxs-lookup"><span data-stu-id="e37f9-137">Complete</span></span></th>
<th><span data-ttu-id="e37f9-138">Autt</span><span class="sxs-lookup"><span data-stu-id="e37f9-138">Empty</span></span></th>
<th><span data-ttu-id="e37f9-139">Búa til tilvikskanban</span><span class="sxs-lookup"><span data-stu-id="e37f9-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e37f9-140">Flytja</span><span class="sxs-lookup"><span data-stu-id="e37f9-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="e37f9-141">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="e37f9-141">Not planned</span></span></li>
<li><span data-ttu-id="e37f9-142">Engin föst vinnsla eða fastar vinnslur eru loknar</span><span class="sxs-lookup"><span data-stu-id="e37f9-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="e37f9-143">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-143">Yes</span></span></td>
<td><span data-ttu-id="e37f9-144">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-144">Yes</span></span></td>
<td><span data-ttu-id="e37f9-145">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-145">Yes</span></span></td>
<td><span data-ttu-id="e37f9-146">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-146">Yes</span></span></td>
<td><span data-ttu-id="e37f9-147">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-147">No</span></span></td>
<td><span data-ttu-id="e37f9-148">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e37f9-149">Flytja</span><span class="sxs-lookup"><span data-stu-id="e37f9-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="e37f9-150">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="e37f9-150">Not planned</span></span></li>
<li><span data-ttu-id="e37f9-151">Föstu vinnslunni er ekki Lokið</span><span class="sxs-lookup"><span data-stu-id="e37f9-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="e37f9-152">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-152">Yes</span></span></td>
<td><span data-ttu-id="e37f9-153">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-153">No</span></span></td>
<td><span data-ttu-id="e37f9-154">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-154">Yes</span></span></td>
<td><span data-ttu-id="e37f9-155">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-155">No</span></span></td>
<td><span data-ttu-id="e37f9-156">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-156">No</span></span></td>
<td><span data-ttu-id="e37f9-157">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e37f9-158">Flytja</span><span class="sxs-lookup"><span data-stu-id="e37f9-158">Transfer</span></span></td>
<td><span data-ttu-id="e37f9-159">Í gangi</span><span class="sxs-lookup"><span data-stu-id="e37f9-159">In progress</span></span></td>
<td><span data-ttu-id="e37f9-160">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-160">Yes</span></span></td>
<td><span data-ttu-id="e37f9-161">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-161">No</span></span></td>
<td><span data-ttu-id="e37f9-162">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-162">Yes</span></span></td>
<td><span data-ttu-id="e37f9-163">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-163">Yes</span></span></td>
<td><span data-ttu-id="e37f9-164">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-164">No</span></span></td>
<td><span data-ttu-id="e37f9-165">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e37f9-166">Flytja</span><span class="sxs-lookup"><span data-stu-id="e37f9-166">Transfer</span></span></td>
<td><span data-ttu-id="e37f9-167">Lokið</span><span class="sxs-lookup"><span data-stu-id="e37f9-167">Completed</span></span></td>
<td><span data-ttu-id="e37f9-168">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-168">No</span></span></td>
<td><span data-ttu-id="e37f9-169">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-169">No</span></span></td>
<td><span data-ttu-id="e37f9-170">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-170">No</span></span></td>
<td><span data-ttu-id="e37f9-171">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-171">No</span></span></td>
<td><span data-ttu-id="e37f9-172">Já</span><span class="sxs-lookup"><span data-stu-id="e37f9-172">Yes</span></span></td>
<td><span data-ttu-id="e37f9-173">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e37f9-174">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="e37f9-174">Transfer or process</span></span></td>
<td><span data-ttu-id="e37f9-175">Autt</span><span class="sxs-lookup"><span data-stu-id="e37f9-175">Empty</span></span></td>
<td><span data-ttu-id="e37f9-176">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-176">No</span></span></td>
<td><span data-ttu-id="e37f9-177">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-177">No</span></span></td>
<td><span data-ttu-id="e37f9-178">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-178">No</span></span></td>
<td><span data-ttu-id="e37f9-179">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-179">No</span></span></td>
<td><span data-ttu-id="e37f9-180">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-180">No</span></span></td>
<td><span data-ttu-id="e37f9-181">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e37f9-182">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="e37f9-182">Transfer or process</span></span></td>
<td><span data-ttu-id="e37f9-183">Kanban-spjald finnst ekki</span><span class="sxs-lookup"><span data-stu-id="e37f9-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="e37f9-184">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-184">No</span></span></td>
<td><span data-ttu-id="e37f9-185">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-185">No</span></span></td>
<td><span data-ttu-id="e37f9-186">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-186">No</span></span></td>
<td><span data-ttu-id="e37f9-187">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-187">No</span></span></td>
<td><span data-ttu-id="e37f9-188">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-188">No</span></span></td>
<td><span data-ttu-id="e37f9-189">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e37f9-190">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="e37f9-190">Transfer or process</span></span></td>
<td><span data-ttu-id="e37f9-191">Kanban-spjald finnst, en það er ekki úthlutuð til kanban</span><span class="sxs-lookup"><span data-stu-id="e37f9-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="e37f9-192">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-192">No</span></span></td>
<td><span data-ttu-id="e37f9-193">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-193">No</span></span></td>
<td><span data-ttu-id="e37f9-194">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-194">No</span></span></td>
<td><span data-ttu-id="e37f9-195">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-195">No</span></span></td>
<td><span data-ttu-id="e37f9-196">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-196">No</span></span></td>
<td><span data-ttu-id="e37f9-197">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e37f9-198">Ferli</span><span class="sxs-lookup"><span data-stu-id="e37f9-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="e37f9-199">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="e37f9-199">Not planned</span></span></li>
<li><span data-ttu-id="e37f9-200">Undirbúið</span><span class="sxs-lookup"><span data-stu-id="e37f9-200">Prepared</span></span></li>
<li><span data-ttu-id="e37f9-201">Í gangi</span><span class="sxs-lookup"><span data-stu-id="e37f9-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="e37f9-202">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-202">No</span></span></td>
<td><span data-ttu-id="e37f9-203">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-203">No</span></span></td>
<td><span data-ttu-id="e37f9-204">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-204">No</span></span></td>
<td><span data-ttu-id="e37f9-205">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-205">No</span></span></td>
<td><span data-ttu-id="e37f9-206">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-206">No</span></span></td>
<td><span data-ttu-id="e37f9-207">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e37f9-208">Ferli</span><span class="sxs-lookup"><span data-stu-id="e37f9-208">Process</span></span></td>
<td><span data-ttu-id="e37f9-209">Lokið</span><span class="sxs-lookup"><span data-stu-id="e37f9-209">Completed</span></span></td>
<td><span data-ttu-id="e37f9-210">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-210">No</span></span></td>
<td><span data-ttu-id="e37f9-211">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-211">No</span></span></td>
<td><span data-ttu-id="e37f9-212">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-212">No</span></span></td>
<td><span data-ttu-id="e37f9-213">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-213">No</span></span></td>
<td><span data-ttu-id="e37f9-214">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-214">No</span></span></td>
<td><span data-ttu-id="e37f9-215">Nei</span><span class="sxs-lookup"><span data-stu-id="e37f9-215">No</span></span></td>
</tr>
</tbody>
</table>





