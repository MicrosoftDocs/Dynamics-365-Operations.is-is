---
title: Sameina þjónustupantanir
description: Þú getur sameinað þjónustupantanir.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bd3ac8cf3c025b082b33247fcd020aebc010bc8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247719"
---
# <a name="combine-service-orders"></a>Sameina þjónustupantanir   

[!include [banner](../includes/banner.md)]


Þegar þú stofnar þjónustupantanalínur sjálfkrafa í **þjónustusamningunum** skjámynd getur þú valið einn af eftirfarandi valkostum til að tilgreina hvernig þú vilt flokka þær:

  - **Eftir þjónustusamningum**

  - **Eftir þjónustuverk**

  - **Eftir starfsmönnum**

  - **Eftir þjónustuhlutum**

## <a name="example"></a>Dæmi

Þú stofnar þjónustusamning sem hefur upphafsdag þann 03-31-2007. Í **Sameina þjónustupantanir** reitinn tilgreinir þú **Eftir þjónustuhlut**. Svo eru eftirfarandi þjónustusamningslínur stofnaðar:

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Samningslínunúmer</p></th>
<th><p>Færslugerð</p></th>
<th><p>lýsing</p></th>
<th><p>Bil</p></th>
<th><p>Þjónustuhlutur</p></th>
<th><p>Fyrsti vinnudagur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Vinnustund</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Vikulega</p></td>
<td><p>X-1</p></td>
<td><p>01-04-2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Vinnustund</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Aðra hverja viku</p></td>
<td><p>X-2</p></td>
<td><p>01-04-2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Vinnustund</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Vikulega</p></td>
<td><p>X-2</p></td>
<td><p>01-04-2007</p></td>
</tr>
</tbody>
</table>


Ekki eru skilgreindir tímagluggar fyrir neina af þjónustupöntunarlínunum. Þess vegna munu þjónustupöntunarlínurnar ekki færast frá þeim reiknaða degi sem þær raðast niður á.

Næst býrðu til þjónustupantanalínur frá **Búa til þjónustupantanir** skjámynd frá 04-01-2007 til 04-30-2007.

Í allt eru 10 þjónustupantanir stofnaðar. Vegna þess að sameinaða stillingin sem þú valdir var **Eftir þjónustuhlut** eru allar þjónustupantanir sem eru búnar til aðeins með þjónustupantanalínur með eina tiltekna þjónustuhlut. Þjónustupantanalínur sem búnar eru til úr þjónustusamningi og hafa sömu þjónustudagsetningu og hlut er sameinuð á sömu þjónustustigi.


> [!NOTE]
> <P>Í þessu dæmi er dagatalið sem er tilgreint í <STRONG>Færibreytur þjónustukerfis</STRONG> skjámynd ekki með neina lokaðir dagar.</P>



Viðbótar flokkun þjónustupantanalína í þjónustupantanir fer fram í samræmi við hvaða tímaglugga sem þú tilgreinir á þjónustusamningslínum.

## <a name="see-also"></a>Sjá einnig

[Stofna þjónustupantanir sjálfkrafa](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]