---
title: Stuðningur við Kanban-flutningsbretti fyrir strikamerkjaskanna
description: Flutningstafla kanbans styður skönnun frá smátóls (widget) strikamerkjaskanna til að Velja, Hefja, Ljúka og Tæma kanban-vinnslu.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b18aad4dcdbf8c2d18960ae306556c3ea679d622
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566812"
---
# <a name="kanban-transfer-board-support-for-bar-code-scanners"></a>Stuðningur við Kanban-flutningsbretti fyrir strikamerkjaskanna

[!include [banner](../includes/banner.md)]

Flutningstafla kanbans styður skönnun frá smátóls (widget) strikamerkjaskanna til að Velja, Hefja, Ljúka og Tæma kanban-vinnslu.

## <a name="registration-modes"></a>Skráningarhamar

Á **skráning Skanna** flýtiflipa er hægt að velja skráningarham sem stýrir aðgerðinni þegar kanban-spjaldnúmer er skannað eða númerið slegið handvirkt inn í númerareit kanban-spjalds.

| Stilla skráningarham | Lýsing                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Hefja                 | Skrá flutningsvinnslu kanbans sem í vinnslu                                                 |
| Frágengið              | Skrá flutningsvinnslu kanbans sem lokið                                                   |
| Autt                 | Skráir efnismeðhöndlunareininguna sem kanban-kort vísar í sem tóma              |
| Velja                | Skráir númer kanban-spjalds og velja vinnsluna sem vísað var í sjálfkrafa í kanban-lista |

 
## <a name="registration-mode-select"></a>Velja skráningarham

Þegar notaður er strikamerkjaalesari til að velja vinnslu, breytist birtingarhamur kanban-spjalds. Í þessari stillingu gilda eftirfarandi skilyrði:

-   Aðeins skannaðs kanban-vinnslu birtist.
-   Upplýsingar um valið verk eru birtar í **upplýsingar** flýtiflipanum.
-   **Skilaboð** flýtiflipi birtir skilaboð aðeins fyrir valda vinnslu.
-   Hægt er að breyta stöðu vinnslunnar með því að nota eiginleika sem eru tiltækir í Aðgerðarúðunni. Flutningstafla Kanbans heldur áfram til að birta aðeins einni vinnslu við þessa tíma.
-   Hægt er að uppfæra upplýsingar í lista yfir vinnslur handvirkt með því að smella **Endurnýja** (Shift + F5) á við Aðgerðasvæði. Eftir að þú endurnýjar upplýsingarnar birtast fullar niðurstöður fyrir síu vinnslu aftur.

## <a name="job-status-and-possible-actions"></a>Staða vinnslu og mögulegar aðgerðir
Staða valinnar vinnslu og stöðuna á öllum föstum vinnslum fyrir tilvik kanbans, ákvarða hvort hægt sé að vinna vinnsluna frekar. Eftirfarandi tafla birtir upplýsingar um þessar stöður og vinnslur:
-   Stöður sem eru tiltæk fyrir vinnslur eða efnismeðhöndlunareiningar sem er vísað í úr vinnslunum.
-   Hvert verk sem hægt er að framkvæma fyrir vinnslu.

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
<th>Vinnslugerð</th>
<th>Staða Vinnslu eða staða efnismeðhöndlunareiningar</th>
<th>Uppfæra tiltektarlista</th>
<th>Hefja</th>
<th>Uppfæra skráningu</th>
<th>Frágengið</th>
<th>Autt</th>
<th>Búa til tilvikskanban</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Flytja</td>
<td><ul>
<li>Ekki áætlað</li>
<li>Engin föst vinnsla eða fastar vinnslur eru loknar</li>
</ul></td>
<td>Já</td>
<td>Já</td>
<td>Já</td>
<td>Já</td>
<td>Nei</td>
<td>Já</td>
</tr>
<tr class="even">
<td>Flytja</td>
<td><ul>
<li>Ekki áætlað</li>
<li>Föstu vinnslunni er ekki Lokið</li>
</ul></td>
<td>Já</td>
<td>Nei</td>
<td>Já</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
</tr>
<tr class="odd">
<td>Flytja</td>
<td>Í gangi</td>
<td>Já</td>
<td>Nei</td>
<td>Já</td>
<td>Já</td>
<td>Nei</td>
<td>Nei</td>
</tr>
<tr class="even">
<td>Flytja</td>
<td>Lokið</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Já</td>
<td>Nei</td>
</tr>
<tr class="odd">
<td>Flutningur eða ferli</td>
<td>Autt</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
</tr>
<tr class="even">
<td>Flutningur eða ferli</td>
<td>Kanban-spjald finnst ekki</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
</tr>
<tr class="odd">
<td>Flutningur eða ferli</td>
<td>Kanban-spjald finnst, en það er ekki úthlutuð til kanban</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
</tr>
<tr class="even">
<td>Ferli</td>
<td><ul>
<li>Ekki áætlað</li>
<li>Undirbúið</li>
<li>Í gangi</li>
</ul></td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
</tr>
<tr class="odd">
<td>Ferli</td>
<td>Lokið</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
<td>Nei</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]