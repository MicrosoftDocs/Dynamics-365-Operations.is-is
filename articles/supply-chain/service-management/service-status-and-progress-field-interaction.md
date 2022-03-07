---
title: Svæðavirkni stöðu og ferlis þjónustu
description: Í skjámynd þjónustupantana endurspeglar framvindureitinn á hausnum stöðu allrar þjónustupöntunarinnar, og „Staða“ skýrir stöðu einstakra þjónustupöntunarlína.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0758c370fd1548770d596115b18f133071f3bbc0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566096"
---
# <a name="service-status-and-progress-field-interaction"></a>Svæðavirkni stöðu og ferlis þjónustu

[!include [banner](../includes/banner.md)]

Í skjámyndinni **Þjónustupantanir** endurspeglar reiturinn **Framvinda** á haus þjónustupöntunar stöðu allrar þjónustupöntunarinnar, og **Staða** skýrir stöðu einstakra þjónustupöntunarlína.

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Framvinda</p></th>
<th><p>Staða línu 1</p></th>
<th><p>Staða línu 2</p></th>
<th><p>Staða línu 3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Í vinnslu</strong></p></td>
<td><p><strong>Stofnað</strong></p></td>
<td><p><strong>Stofnað</strong></p></td>
<td><p><strong>Stofnað</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Í vinnslu</strong></p></td>
<td><p><strong>Hætt við</strong></p></td>
<td><p><strong>Stofnað</strong></p></td>
<td><p><strong>Stofnað</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Í vinnslu</strong></p></td>
<td><p><strong>Stofnað</strong></p></td>
<td><p><strong>Hætt við</strong></p></td>
<td><p><strong>Birt</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Hætt við</strong></p></td>
<td><p><strong>Hætt við</strong></p></td>
<td><p><strong>Hætt við</strong></p></td>
<td><p><strong>Hætt við</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Birt</strong></p></td>
<td><p><strong>Birt</strong></p></td>
<td><p><strong>Birt</strong></p></td>
<td><p><strong>Birt</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Birt</strong></p></td>
<td><p><strong>Birt</strong></p></td>
<td><p><strong>Hætt við</strong></p></td>
<td><p><strong>Hætt við</strong></p></td>
</tr>
</tbody>
</table>

Framvinda þjónustupöntunar er í gangi ef allar línur hafa stöðuna **Stofnað**; hún er enn í vinnslu ef einhverjar af línunum hafa stöðuna **Hætt við** eða **Bókað**.

Ef allar línur í þjónustupöntun eru merktar sem **Bókað** er framvinda pöntunarstöðu **Bókað**. Ef einhverjar línur eru **Bókað** og sumar eru **Hætt við** er framvindan enn **Bókað**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
