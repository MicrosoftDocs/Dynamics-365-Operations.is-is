---
title: Svæðavirkni stöðu og ferlis þjónustu
description: Í skjámynd þjónustupantana endurspeglar framvindureitinn á hausnum stöðu allrar þjónustupöntunarinnar, og „Staða“ skýrir stöðu einstakra þjónustupöntunarlína.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207325"
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

  


