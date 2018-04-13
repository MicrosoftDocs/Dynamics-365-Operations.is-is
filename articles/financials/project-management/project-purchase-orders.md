---
title: Innkaupapantanir fyrir verk
description: "Þessi grein lýsir ýmsum aðferðum sem hægt er að nota til að stofna innkaupapantanir fyrir verk. Aðferðin sem notuð er er háð tilgangi innkaupapöntunar, og þegar keyptar vörur eru notaðar og innheimtar á verk."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: dae65394a2180ccbf3317a41b635ba97034e541b
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="purchase-orders-for-a-project"></a>Innkaupapantanir fyrir verk

[!INCLUDE [banner](../includes/banner.md)]

Þessi grein lýsir ýmsum aðferðum sem hægt er að nota til að stofna innkaupapantanir fyrir verk. Aðferðin sem notuð er er háð tilgangi innkaupapöntunar, og þegar keyptar vörur eru notaðar og innheimtar á verk.

Í Microsoft Dynamics 365 for Finance and Operations er hægt að nota margar aðferðir til að stofna innkaupapantanir fyrir verk. Aðferðin sem notuð er er háð tilgangi innkaupapöntunar, þegar keyptar vörur eru notaðar og þegar keyptar vörur eru reikningsfærðar á verk.

### <a name="methods-for-creating-a-purchase-order"></a>Aðferðir til að búa til innkaupapöntun

Hægt er að nota eina af eftirfarandi aðferðum til að stofna innkaupapöntun í Verkefnastjórnun og bókhald. Tilgangur innkaupapöntunar ákvarðar hvenær innkaupapöntunin er notuð og þar með hvenær vörur eru innheimtar á verk.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Aðferð</th>
<th>Tilgangur</th>
<th>Notkun vara</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stofna innkaupapöntun beint úr verki.</td>
<td>Notið þessa aðferð til að kaupa inn vörur frá ytri lánardrottni fyrir notkun í verki. Hægt er að stofna innkaupapöntun á tvo vegu:
<ul>
<li>Frá verkinu sjálfu. Í þessu tilfelli hefur verkið þegar verið tilgreint fyrir innkaupapöntunina.</li>
<li>Með því að fletta að verkið innkaupapöntun. Velja þarf bæði lánardrottinn og verk sem stofna á innkaupapöntun fyrir.</li>
</ul></td>
<td>Vörur eru notaðar þegar reikningur lánardrottins er uppfærður.</td>
</tr>
<tr class="even">
<td>Stofna innkaupapöntun úr sölupöntun</td>
<td>Notið þessa aðferð til að kaupa vörur þegar sölupöntun er stofnuð úr verki.</td>
<td>Vörur eru notaðar þegar sölupöntun er reikningsfærð til viðskiptavinar.</td>
</tr>
<tr class="odd">
<td>Stofnið innkaupapöntun úr vöruþörf.</td>
<td>Notið þessa aðferð til að kaupa vörur þegar vöruþörf er stofnuð úr verki.</td>
<td>Vörur eru notaðar þegar fylgiseðill vöruþarfar er uppfærður.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Þegar reikningur lánardrottins eða fylgiseðill er uppfærður ertu hvattur til að uppfæra fylgiseðilinn í vöruþörf.

Frekari upplýsingar, sjá [Fá vörur úr innkaupapöntun frá vöruþörf](tasks/receive-items-purchase-order-item-requirement.md).


