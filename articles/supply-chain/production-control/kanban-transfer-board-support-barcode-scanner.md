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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1dc40de2b77be5c5c2399fd55c3c3bd15a9f24ec
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="bd5c7-103">Stuðningur við Kanban-flutningsbretti fyrir strikamerkjaskanna</span><span class="sxs-lookup"><span data-stu-id="bd5c7-103">Kanban transfer board support for barcode scanners</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bd5c7-104">Flutningstafla kanbans styður skönnun frá smátóls (widget) strikamerkjaskanna til að Velja, Hefja, Ljúka og Tæma kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="bd5c7-105">Skráningarhamar</span><span class="sxs-lookup"><span data-stu-id="bd5c7-105">Registration modes</span></span>
------------------

<span data-ttu-id="bd5c7-106">Á **skráning Skanna** flýtiflipa er hægt að velja skráningarham sem stýrir aðgerðinni þegar kanban-spjaldnúmer er skannað eða númerið slegið handvirkt inn í númerareit kanban-spjalds.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>
| <span data-ttu-id="bd5c7-107">Stilla skráningarham</span><span class="sxs-lookup"><span data-stu-id="bd5c7-107">Set registration mode</span></span> | <span data-ttu-id="bd5c7-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="bd5c7-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5c7-109">Hefja</span><span class="sxs-lookup"><span data-stu-id="bd5c7-109">Start</span></span>                 | <span data-ttu-id="bd5c7-110">Skrá flutningsvinnslu kanbans sem í vinnslu</span><span class="sxs-lookup"><span data-stu-id="bd5c7-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="bd5c7-111">Frágengið</span><span class="sxs-lookup"><span data-stu-id="bd5c7-111">Complete</span></span>              | <span data-ttu-id="bd5c7-112">Skrá flutningsvinnslu kanbans sem lokið</span><span class="sxs-lookup"><span data-stu-id="bd5c7-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="bd5c7-113">Autt</span><span class="sxs-lookup"><span data-stu-id="bd5c7-113">Empty</span></span>                 | <span data-ttu-id="bd5c7-114">Skráir efnismeðhöndlunareininguna sem kanban-kort vísar í sem tóma</span><span class="sxs-lookup"><span data-stu-id="bd5c7-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="bd5c7-115">Velja</span><span class="sxs-lookup"><span data-stu-id="bd5c7-115">Select</span></span>                | <span data-ttu-id="bd5c7-116">Skráir númer kanban-spjalds og velja vinnsluna sem vísað var í sjálfkrafa í kanban-lista</span><span class="sxs-lookup"><span data-stu-id="bd5c7-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="bd5c7-117">Velja skráningarham</span><span class="sxs-lookup"><span data-stu-id="bd5c7-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="bd5c7-118">Þegar notaður er strikamerkjaalesari til að velja vinnslu, breytist birtingarhamur kanban-spjalds.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="bd5c7-119">Í þessari stillingu gilda eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="bd5c7-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="bd5c7-120">Aðeins skannaðs kanban-vinnslu birtist.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="bd5c7-121">Upplýsingar um valið verk eru birtar í **upplýsingar** flýtiflipanum.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="bd5c7-122">**Skilaboð** flýtiflipi birtir skilaboð aðeins fyrir valda vinnslu.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="bd5c7-123">Hægt er að breyta stöðu vinnslunnar með því að nota eiginleika sem eru tiltækir í Aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="bd5c7-124">Flutningstafla Kanbans heldur áfram til að birta aðeins einni vinnslu við þessa tíma.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="bd5c7-125">Hægt er að uppfæra upplýsingar í lista yfir vinnslur handvirkt með því að smella **Endurnýja** (Shift + F5) á við Aðgerðasvæði.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="bd5c7-126">Eftir að þú endurnýjar upplýsingarnar birtast fullar niðurstöður fyrir síu vinnslu aftur.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="bd5c7-127">Staða vinnslu og mögulegar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="bd5c7-127">Job status and possible actions</span></span>
<span data-ttu-id="bd5c7-128">Staða valinnar vinnslu og stöðuna á öllum föstum vinnslum fyrir tilvik kanbans, ákvarða hvort hægt sé að vinna vinnsluna frekar.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="bd5c7-129">Eftirfarandi tafla birtir upplýsingar um þessar stöður og vinnslur:</span><span class="sxs-lookup"><span data-stu-id="bd5c7-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="bd5c7-130">Stöður sem eru tiltæk fyrir vinnslur eða efnismeðhöndlunareiningar sem er vísað í úr vinnslunum.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="bd5c7-131">Hvert verk sem hægt er að framkvæma fyrir vinnslu.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="bd5c7-132">Vinnslugerð</span><span class="sxs-lookup"><span data-stu-id="bd5c7-132">Job type</span></span></th>
<th><span data-ttu-id="bd5c7-133">Staða Vinnslu eða staða efnismeðhöndlunareiningar</span><span class="sxs-lookup"><span data-stu-id="bd5c7-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="bd5c7-134">Uppfæra tiltektarlista</span><span class="sxs-lookup"><span data-stu-id="bd5c7-134">Update picking list</span></span></th>
<th><span data-ttu-id="bd5c7-135">Hefja</span><span class="sxs-lookup"><span data-stu-id="bd5c7-135">Start</span></span></th>
<th><span data-ttu-id="bd5c7-136">Uppfæra skráningu</span><span class="sxs-lookup"><span data-stu-id="bd5c7-136">Update registration</span></span></th>
<th><span data-ttu-id="bd5c7-137">Frágengið</span><span class="sxs-lookup"><span data-stu-id="bd5c7-137">Complete</span></span></th>
<th><span data-ttu-id="bd5c7-138">Autt</span><span class="sxs-lookup"><span data-stu-id="bd5c7-138">Empty</span></span></th>
<th><span data-ttu-id="bd5c7-139">Búa til tilvikskanban</span><span class="sxs-lookup"><span data-stu-id="bd5c7-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd5c7-140">Flytja</span><span class="sxs-lookup"><span data-stu-id="bd5c7-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="bd5c7-141">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="bd5c7-141">Not planned</span></span></li>
<li><span data-ttu-id="bd5c7-142">Engin föst vinnsla eða fastar vinnslur eru loknar</span><span class="sxs-lookup"><span data-stu-id="bd5c7-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="bd5c7-143">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-143">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-144">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-144">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-145">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-145">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-146">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-146">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-147">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-147">No</span></span></td>
<td><span data-ttu-id="bd5c7-148">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd5c7-149">Flytja</span><span class="sxs-lookup"><span data-stu-id="bd5c7-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="bd5c7-150">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="bd5c7-150">Not planned</span></span></li>
<li><span data-ttu-id="bd5c7-151">Föstu vinnslunni er ekki Lokið</span><span class="sxs-lookup"><span data-stu-id="bd5c7-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="bd5c7-152">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-152">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-153">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-153">No</span></span></td>
<td><span data-ttu-id="bd5c7-154">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-154">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-155">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-155">No</span></span></td>
<td><span data-ttu-id="bd5c7-156">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-156">No</span></span></td>
<td><span data-ttu-id="bd5c7-157">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd5c7-158">Flytja</span><span class="sxs-lookup"><span data-stu-id="bd5c7-158">Transfer</span></span></td>
<td><span data-ttu-id="bd5c7-159">Í gangi</span><span class="sxs-lookup"><span data-stu-id="bd5c7-159">In progress</span></span></td>
<td><span data-ttu-id="bd5c7-160">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-160">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-161">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-161">No</span></span></td>
<td><span data-ttu-id="bd5c7-162">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-162">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-163">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-163">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-164">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-164">No</span></span></td>
<td><span data-ttu-id="bd5c7-165">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd5c7-166">Flytja</span><span class="sxs-lookup"><span data-stu-id="bd5c7-166">Transfer</span></span></td>
<td><span data-ttu-id="bd5c7-167">Lokið</span><span class="sxs-lookup"><span data-stu-id="bd5c7-167">Completed</span></span></td>
<td><span data-ttu-id="bd5c7-168">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-168">No</span></span></td>
<td><span data-ttu-id="bd5c7-169">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-169">No</span></span></td>
<td><span data-ttu-id="bd5c7-170">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-170">No</span></span></td>
<td><span data-ttu-id="bd5c7-171">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-171">No</span></span></td>
<td><span data-ttu-id="bd5c7-172">Já</span><span class="sxs-lookup"><span data-stu-id="bd5c7-172">Yes</span></span></td>
<td><span data-ttu-id="bd5c7-173">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd5c7-174">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="bd5c7-174">Transfer or process</span></span></td>
<td><span data-ttu-id="bd5c7-175">Autt</span><span class="sxs-lookup"><span data-stu-id="bd5c7-175">Empty</span></span></td>
<td><span data-ttu-id="bd5c7-176">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-176">No</span></span></td>
<td><span data-ttu-id="bd5c7-177">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-177">No</span></span></td>
<td><span data-ttu-id="bd5c7-178">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-178">No</span></span></td>
<td><span data-ttu-id="bd5c7-179">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-179">No</span></span></td>
<td><span data-ttu-id="bd5c7-180">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-180">No</span></span></td>
<td><span data-ttu-id="bd5c7-181">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd5c7-182">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="bd5c7-182">Transfer or process</span></span></td>
<td><span data-ttu-id="bd5c7-183">Kanban-spjald finnst ekki</span><span class="sxs-lookup"><span data-stu-id="bd5c7-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="bd5c7-184">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-184">No</span></span></td>
<td><span data-ttu-id="bd5c7-185">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-185">No</span></span></td>
<td><span data-ttu-id="bd5c7-186">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-186">No</span></span></td>
<td><span data-ttu-id="bd5c7-187">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-187">No</span></span></td>
<td><span data-ttu-id="bd5c7-188">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-188">No</span></span></td>
<td><span data-ttu-id="bd5c7-189">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd5c7-190">Flutningur eða ferli</span><span class="sxs-lookup"><span data-stu-id="bd5c7-190">Transfer or process</span></span></td>
<td><span data-ttu-id="bd5c7-191">Kanban-spjald finnst, en það er ekki úthlutuð til kanban</span><span class="sxs-lookup"><span data-stu-id="bd5c7-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="bd5c7-192">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-192">No</span></span></td>
<td><span data-ttu-id="bd5c7-193">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-193">No</span></span></td>
<td><span data-ttu-id="bd5c7-194">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-194">No</span></span></td>
<td><span data-ttu-id="bd5c7-195">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-195">No</span></span></td>
<td><span data-ttu-id="bd5c7-196">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-196">No</span></span></td>
<td><span data-ttu-id="bd5c7-197">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd5c7-198">Ferli</span><span class="sxs-lookup"><span data-stu-id="bd5c7-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="bd5c7-199">Ekki áætlað</span><span class="sxs-lookup"><span data-stu-id="bd5c7-199">Not planned</span></span></li>
<li><span data-ttu-id="bd5c7-200">Undirbúið</span><span class="sxs-lookup"><span data-stu-id="bd5c7-200">Prepared</span></span></li>
<li><span data-ttu-id="bd5c7-201">Í gangi</span><span class="sxs-lookup"><span data-stu-id="bd5c7-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="bd5c7-202">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-202">No</span></span></td>
<td><span data-ttu-id="bd5c7-203">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-203">No</span></span></td>
<td><span data-ttu-id="bd5c7-204">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-204">No</span></span></td>
<td><span data-ttu-id="bd5c7-205">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-205">No</span></span></td>
<td><span data-ttu-id="bd5c7-206">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-206">No</span></span></td>
<td><span data-ttu-id="bd5c7-207">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd5c7-208">Ferli</span><span class="sxs-lookup"><span data-stu-id="bd5c7-208">Process</span></span></td>
<td><span data-ttu-id="bd5c7-209">Lokið</span><span class="sxs-lookup"><span data-stu-id="bd5c7-209">Completed</span></span></td>
<td><span data-ttu-id="bd5c7-210">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-210">No</span></span></td>
<td><span data-ttu-id="bd5c7-211">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-211">No</span></span></td>
<td><span data-ttu-id="bd5c7-212">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-212">No</span></span></td>
<td><span data-ttu-id="bd5c7-213">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-213">No</span></span></td>
<td><span data-ttu-id="bd5c7-214">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-214">No</span></span></td>
<td><span data-ttu-id="bd5c7-215">Nei</span><span class="sxs-lookup"><span data-stu-id="bd5c7-215">No</span></span></td>
</tr>
</tbody>
</table>






