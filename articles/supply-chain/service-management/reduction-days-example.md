---
title: "Dæmi um minnkunardaga"
description: "Dæmi um minnkunardaga."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69e4b1b0fe100b17e5b2c59be81604019347956f
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---


# <a name="reduction-days-example"></a>Dæmi um minnkunardaga 

[!include [banner](../includes/banner.md)]


Þú hefur búið til áskriftrarfærslu fyrir viðhaldsáskrift viðskiptavinar, eins og lýst er í eftirfarandi töflu.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Dagsetning frá</p></th>
<th><p>Dagsetning til</p></th>
<th><p>Áskrift</p></th>
<th><p>Gerð áskriftar</p></th>
<th><p>Verkefni</p></th>
<th><p>Tegund</p></th>
<th><p>Sölugjaldmiðill</p></th>
<th><p>Söluverð</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01. mars, 2011</p></td>
<td><p>31. mars, 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Venjuleg</strong></p></td>
<td><p>9013</p></td>
<td><p>Undirteg2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Viðskiptavinurinn tilkynnir að hann þurfi ekki þjónustuþekju í tvo daga (10. mars og 11. mars). Þú samþykkir að stytta áskriftina sem nemur þessum tveimur dögum.

Þú býrð til nýja færslu af gerðinni **Minnkunardagar** eins og lýst er í eftirfarandi töflu.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Dagsetning frá</p></th>
<th><p>Dagsetning til</p></th>
<th><p>Áskrift</p></th>
<th><p>Gerð áskriftar</p></th>
<th><p>Verkefni</p></th>
<th><p>Tegund</p></th>
<th><p>Sölugjaldmiðill</p></th>
<th><p>Söluverð</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10. mars, 2011</p></td>
<td><p>11. mars, 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Lækkunardagar</strong></p></td>
<td><p>9013</p></td>
<td><p>Undirteg2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


Þegar færslur fyrir mars 2011 eru reikningsfærðar er söluverðið EUR 200 lækkað um EUR 12.90. Reikningshæf upphæð fyrir áskriftarfærsluna er þar af leiðandi EUR 187.10, og tvær færslur eru reikningsfærðar fyrir samtals EUR 187.10.

## <a name="see-also"></a>Sjá einnig

[Fækka dögum á áskrifarþóknunum](reduce-the-days-on-subscription-fees.md)

  



