---
title: "Birgðagildi hlut"
description: "Þessi grein veitir upplýsingar um hvernig gildi birgðahlutar eru reiknuð."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Birgðagildi hlut

Þessi grein veitir upplýsingar um hvernig gildi birgðahlutar eru reiknuð. 

Nýrri aðgerð sem kallast ** efnislegt magn ** gerir það mögulegt að sjá gildi hlutarins tilteknar birgðir. Kostnaðarhlutur táknar einingarstig þar sem birgðabókhald er framkvæmt. Nánari upplýsingar um kostnaðarhluti er í [Kostnaðarhlutir](cost-object.md). Til að sjá gildi hlutarins tilteknar birgðir, smellið á **Efnislegt magn** í í **Kostnaður hlut** síðu. Hér er hvernig gildi hlut birgða er reiknað: Birgðir hlut. Virði = Kostnaður hlut. Meðaltal einingarkostnað × Birgðir hlut. Magn Sem eftirfarandi dæmi sýnir hvernig gildi hlut birgða og kostnaður hlutar eru reiknaðar. Tvö innhreyfingarskjöl afurða eru skráð á vöru A:

-   Innhreyfingarskjal afurða 1: Magn = 100 pc-tölva., Upphæð = $1,000.00, Svæði = 1, Vöruhús = 11, nr. Runu = B1
-   Innhreyfingarskjal afurða 2: Magn = 50 pc-tölva., Upphæð = $800.00, Svæði = 1, Vöruhús = 11, Runa nr. = B2

Eftirfarandi tafla sýnir niðurstöður útreiknings fyrir kostnaðarhlut. Hægt er að skoða niðurstöður á síðunni **Kostnaðarhlutur**.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Gerð hlutar</th>
<th>Vörunúmer</th>
<th>Svæði</th>
<th>Magn</th>
<th>Birgðaeining</th>
<th>Gildi</th>
<th>Meðaleiningarkostnaður</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kostnaðarhlutur</td>
<td>Lista fyrir</td>
<td>1</td>
<td>150</td>
<td>Stk.</td>
<td><p>$1800,00</p></td>
<td><p>$12,00</p></td>
</tr>
</tbody>
</table>

Eftirfarandi tafla sýnir niðurstöður útreiknings fyrir birgðahlut. Hægt er að skoða niðurstöðurnar með því að smella á **Efnislegt magn** á síðunni **Kostnaðarhlutur**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Gerð hlutar</th>
<th>Vörunúmer</th>
<th>Svæði</th>
<th>Vöruhús</th>
<th>Rununr.</th>
<th>Magn</th>
<th>Birgðaeining</th>
<th>Gildi</th>
<th>Meðaleiningarkostnaður</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Birgðahlutur</td>
<td>Lista fyrir</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Stk.</td>
<td><p>$1200.00</p></td>
<td><p>$12,00</p></td>
</tr>
<tr class="even">
<td>Birgðahlutur</td>
<td>Lista fyrir</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Stk.</td>
<td><p>$600.00</p></td>
<td><p>$12,00</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Sjá einnig
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[Hvað er nýtt og breytt í Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


