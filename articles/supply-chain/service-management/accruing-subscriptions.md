---
title: Safna upp áskriftum
description: Með þjónustuáskriftum er tekjum safnað upp handvirkt á tímabilum sem koma á eftir þeim degi þegar þóknunarfærsla var reikningsfærð.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a183e17749c04b407eb17155ecb1363e96ade18a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "317178"
---
# <a name="accruing-subscriptions"></a>Safna upp áskriftum 

[!include [banner](../includes/banner.md)]


Með þjónustuáskriftum er tekjum safnað upp handvirkt á tímabilum sem koma á eftir þeim degi þegar þóknunarfærsla var reikningsfærð.

Uppsöfnunartímabil eru stofnuð fyrir reikningstímabilið sem sett eru fyrir áskriftarþóknunina, og uppsöfnunartímabilin eru byggð á tímabilskóða áskriftarinnar.

Hægt er að safna upp og bakfæra uppsöfnuðum tekjum.

## <a name="reverse-accruals-of-credit-amounts"></a>Bakfæra uppsafnaðar upphæð inneignar

Ef þú gjaldfærir upphæðir áskriftarreikninga er hægt að nota tvær aðferðir til að bakfæra uppsafnaðri upphæð:

  - Þú getur bakfært hverja uppsöfnuð tekjufærslu fyrir sig, áður en þú býrð til kreditnótutillögu fyrir færsluna. Þetta er handvirka aðferðin. (handvirkt)

  - Þú getur bakfært uppsafnaðar upphæðir á þeim degi sem kreditnótutillagan er bókuð eða á upphaflegu bókunardagsetningu uppsöfnunar.

Nánari upplýsingar er að finna í [Áskriftarbreytur (eyðublað)](https://technet.microsoft.com/en-us/library/aa619615.aspx) .

## <a name="setup-requirements"></a>Setja upp kröfur

Til að safna upp tekjum skaltu ganga úr skugga um að eftirfarandi kröfur um gögn séu uppfyllt:

## <a name="account-setup"></a>Uppsetning lykils

The **WIP - áskrift** og **Uppsafnaðar tekjur - áskrift** reikningarnir verða að vera sett upp í **Verkefni** mátinu.

Þegar þú bókar uppsafnaðar tekjur er **WIP - Áskrift** reikningurinn skuldfærður með uppsöfnunarupphæð og **Uppsafnaðar tekjur - áskrift** reikningurinn gjaldfærður með uppöfnunarupphæð.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Lyklar settir upp fyrir uppsöfnun áskriftartekna

1.  Smelltu á **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Bókun** \> **Uppsetning fjárhagsbókunar**.

2.  Smelltu á **Tekjureikningar** flipann og veldu **WIP - áskrift** eða **Uppsafnaðar tekjur - áskrift** til að setja upp reikningana.

## <a name="subscription-group-setup"></a>Uppsetning áskriftarhópa

Til að hægt sé að safna upp tekjum fyrir áskriftir verður að velja gátreitinn **Safna upp tekjum**. Þetta er að finna á **Áskriftarflokkar** skjámynd fyrir hópinn sem fylgir áskriftinni. Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónusta áskrift** \> **Áskriftarflokkar** .

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Uppsöfnun tekna gerð virk á áskriftarhópi

1.  Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónusta áskrift** \> **Áskriftarflokkar** .

## <a name="periods"></a>Tímabil

Setja verður upp reikningstímabilskóða. Nema þú viljir safna upp tekjum á sama tímabili og þú notar til að reikningsfæra, verður þú einnig að setja upp uppsöfnunartímabil.

Eftirfarandi tafla veitir yfirlit um hvaða uppsöfnunartímabil má setja upp fyrir hvert reikningsfærslutímabil:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tímabil reikningsfærslu</p></th>
<th><p>Uppsöfnunartímabil</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Ár</strong></p></td>
<td><ul>
<li><p><strong>Ár</strong></p></li>
<li><p><strong>Ársfjórðungur</strong></p></li>
<li><p><strong>Mánuður</strong></p></li>
<li><p><strong>Dagur</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Ársfjórðungur</strong></p></td>
<td><ul>
<li><p><strong>Ársfjórðungur</strong></p></li>
<li><p><strong>Mánuður</strong></p></li>
<li><p><strong>Dagur</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Mánuður</strong></p></td>
<td><ul>
<li><p><strong>Mánuður</strong></p></li>
<li><p><strong>Dagur</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Vika</strong></p></td>
<td><ul>
<li><p><strong>Dagur</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Dagur</strong></p></td>
<td><ul>
<li><p><strong>Dagur</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Uppsetning reikningsfærsutímabilsins er lögboðin hluti af heildaruppsetningu áskriftarflokksins. Þú getur ákveðið hvort þú setur einnig upp uppsöfnunartímabil fyrir áskriftarflokkinn. Ef þú setur upp uppsöfnunartímabil fyrir áskriftarflokkinn er þetta tímabil lagt til í **Tímabilskóði** reitinn. Þessi reitur er að finna í **Uppsafnaðar áskriftartekjur** skjámynd, þegar þú safnar upp áskriftartekjur. Uppsöfnunartímabilið er hins vegar valfrjálsar upplýsingar um áskriftarhópinn.


> [!NOTE]
> <P>Notaðu eftirfarandi slóð til að opna <STRONG>Safna upp áskriftartekjum</STRONG> skjámyndina. Smelltu á <STRONG>Þjónustustjórnun</STRONG> &gt; <STRONG>Tímabil</STRONG> &gt; <STRONG>Þjónustuáskriftir</STRONG> &gt; <STRONG>Safna upp áskriftartekjum</STRONG>.</P>


## <a name="transactions"></a>Færslur

Þú getur stjórnað fjölda fjárhagsfærslna sem eru búnar til þegar þú bókar uppsafnaðar tekjur. Á áskriftum skal tilgreina hvort fjárhagsfærslur skuli búin til sem samtala eða á hverja línu.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Tilgreinið stig bókunarupplýsingar sem sýna á fyrir uppsöfnunarfærslur

1.  Smelltu á **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Verkefnastjórnun og bókhaldsfæribreytur**.

2.  Á **Fjármál** flipanum, í reitnum **Reikningur** skal velja **Samtala** eða **Lína**.


## <a name="see-also"></a>Sjá einnig

[Safna upp áskriftartekjum](accrue-subscription-revenue.md)

  


