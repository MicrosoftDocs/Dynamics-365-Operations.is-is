---
title: Gildi birgðahlutar
description: Þessi grein veitir upplýsingar um hvernig gildi birgðahlutar eru reiknuð.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a5dd487b9213f8f1289412a6a7b8112e6b57df6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670385"
---
# <a name="inventory-object-values"></a>Gildi birgðahlutar

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um hvernig gildi birgðahlutar eru reiknuð. 

Ný aðgerð sem kallast **efnislegt magn** gerir það mögulegt að sjá gildi tilgreinds birgðahutar. 

Kostnaðarhlutur táknar einingarstig þar sem birgðabókhald er framkvæmt. Nánari upplýsingar um kostnaðarhluti er í [Kostnaðarhlutir](cost-object.md). 

Til að sjá gildi tiltekins birgðahlutar skal smella á **Efnislegt magn** á síðunni **Kostnaðarhlutur**. Hér er sýnt hvernig gildi birgðahlutar er reiknað: 

Birgðahlutur.Virði = Kostnaðarhlutur.Meðaltal einingarkostnaðar x Birgðahlutur.Magn 

Sem eftirfarandi dæmi sýnir hvernig gildi birgðahlutar og kostnaðarhlutar eru reiknuð. Tvö innhreyfingarskjöl afurða eru skráð á vöru A:

-   Innhreyfingarskjal afurða 1: Magn = 100 stykki, Upphæð = $1000,00, Svæði = 1, Vöruhús = 11, Rununr. = B1
-   Innhreyfingarskjal afurða 2: Magn = 50 stykki, Upphæð = $800,00, Svæði = 1, Vöruhús = 11, Rununr. = B2

Eftirfarandi tafla sýnir niðurstöður útreiknings fyrir kostnaðarhlut. Hægt er að skoða niðurstöður á síðunni **Kostnaðarhlutur**.

<table>
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

<table>
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
<td>A</td>
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



## <a name="additional-resources"></a>Frekari upplýsingar

[Kostnaðarhlutir](cost-object.md)

[Kostnaðarfærslur](cost-entries.md)

[Nýjungar og breytingar](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]