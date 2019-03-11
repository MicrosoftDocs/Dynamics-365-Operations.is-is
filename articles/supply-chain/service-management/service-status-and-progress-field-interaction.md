---
title: Svæðavirkni stöðu og ferlis þjónustu
description: Í skjámynd þjónustupantana endurspeglar framvindureitinn á hausnum stöðu allrar þjónustupöntunarinnar, og „Staða“ skýrir stöðu einstakra þjónustupöntunarlína.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd7b5160149a38dd62535901c1225bf704f404d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "346135"
---
# <a name="service-status-and-progress-field-interaction"></a>Svæðavirkni stöðu og ferlis þjónustu 

[!include [banner](../includes/banner.md)]


Í skjámyndinni **Þjónustupantanir** endurspeglar reiturinn **Framvinda** á haus þjónustupöntunar stöðu allrar þjónustupöntunarinnar, og **Staða** skýrir stöðu einstakra þjónustupöntunarlína.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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

  


