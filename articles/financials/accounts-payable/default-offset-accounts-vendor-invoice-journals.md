---
title: "Sjálfgefnir mótlyklar fyrir reikningsfærslubækur lánardrottna og færslubækur reikningssamþykkta"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4691ac4456b08084bcd93f7a8447719a15299c93
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>Sjálfgefnir mótlyklar fyrir reikningsfærslubækur lánardrottna og færslubækur reikningssamþykkta

[!include[banner](../includes/banner.md)]




Sjálfgefnir mótlyklar eru notaðir á eftirfarandi færslubókarsíðum reiknings lánardrottins:

-   Reikningabók
-   Staðfestingarbók

Eftirfarandi tafla er notuð til að aðstoða við að ákveða hvar á að úthluta sjálfgefnum lyklum fyrir reikningabækur.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Setja upp sjálfgefna lykla hér</th>
<th>Þar sem sjálfgefnir lyklar eru veittir</th>
<th>Hvernig þessi valkostur hefur áhrif á vinnslu</th>
<th>Hvenær á að nota þennan möguleika</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Lánardrottnaflokkur</strong> – Setja upp sjálfgefna mótlykla fyrir flokka lánardrottna á síðunni <strong>Sjálfgefin lykiluppsetning</strong> sem hægt er að opna af síðunni <strong>Lánardrottnaflokkar</strong>.</td>
<td><ul>
<li>Lykill lánardrottins</li>
<li>Færslubókarfærslur fyrir lánardrottnareikninga í lánardrottnahópnum, ef sjálfgefnir reikningar eru ekki tilgreindir fyrir lánardrottnareikninga</li>
</ul></td>
<td>Sjálfgefnir mótlyklar fyrir flokka lánardrottna eru sýndir sem sjálfgefnir mótlyklar fyrir lánardrottna á síðunni <strong>Sjálfgefin lykiluppsetning</strong>. Hægt er að opna þessa síðu af listasíðunni <strong>Allir lánardrottnar</strong>.</td>
<td>Notaðu þennan valkost ef yfirleitt er greitt fyrir sömu gerðir af hlutum úr sömu lánardrottnaflokkum með tímanum.</td>
</tr>
<tr class="even">
<td><strong>Lánardrottnalykill</strong> – Setja upp sjálfgefna lykla fyrir flokka lánardrottna á síðunni <strong>Sjálfgefin lykiluppsetning</strong> sem hægt er að opna af síðunni <strong>Lánardrottnar</strong>.</td>
<td>Færslubókarfærslur fyrir lánardrottnareikning</td>
<td>Sjálfgefnir mótlyklar fyrir lykla lánardrottna eru sýndir sem sjálfgefnir mótlyklar fyrir bókarfærslur fyrir lánardrottnalykilinn.</td>
<td>Notaðu þennan valkost ef yfirleitt er greitt fyrir sömu gerðir af hlutum frá sömu lánardrottnum með tímanum.</td>
</tr>
<tr class="odd">
<td><strong>Færslubókaheiti</strong> – Setja upp sjálfgefna mótlykla fyrir færslubækur á síðunni <strong>Færslubókarheiti</strong>. Velja skal valkostinn <strong>Fastur mótlykill</strong>. Athugaðu að ekki er hægt að tilgreina sjálfgefna mótlykla á færslubókarheiti ef færslubókargerð þeirra er <strong>Komubók</strong> eða <strong>Samþykki</strong>.</td>
<td><ul>
<li>Færslubókarhaus sem notar færslubókarheiti</li>
<li>Færslubókarfærslur í tímaritum sem nota færslubókarheiti</li>
</ul></td>
<td>Ef valkosturinn <strong>Fastur mótlykill</strong> á síðunni <strong>Færslubókaheiti</strong> er valinn, hnekkir mótlykill fyrir færslubókarheiti sjálfgefnum mótlykli fyrir lánardrottinn eða lánardrottnaflokk.</td>
<td>Notið þennan valkost til að setja upp færslubækur fyrir tiltekinn kostnað og kostnað sem er gjaldfærður á tiltekna lykla, án tillits til lánardrottins eða lánardrottnaflokks sem lánardrottinn tilheyrir.</td>
</tr>
<tr class="even">
<td><strong>Færslubókaheiti</strong> – Setja upp sjálfgefna mótlykla fyrir færslubækur á síðunni <strong>Færslubókarheiti</strong>. Hreinsaðu valkostinn <strong>Fastur mótlykill</strong>. Athugaðu að ekki er hægt að tilgreina sjálfgefna mótlykla á færslubókarheiti ef færslubókargerð þeirra er <strong>Komubók</strong> eða <strong>Samþykki</strong>.</td>
<td><ul>
<li>Færslubókarhaus</li>
<li>Færslubókarfærslur í tímaritum sem nota færslubókarheiti</li>
</ul></td>
<td>Þessar sjálfgefnu færslur eru notaðar í færsluhaus á síðum og mótlykill í haus færslubókarsíðu er notaður sem sjálfgefin færsla í fylgiskjali færslubókarsíðna. Sjálfgefnir lyklar af síðunni <strong>Færslubókaheiti </strong>eru aðeins notaðir ef sjálfgefnir lyklar ekki eru uppsettir fyrir lykil lánardrottins.</td>
<td>Notið þennan valkost til að setja upp sjálfgefna lykla sem eru notaðir þegar sjálfgefnum mótlykli lánardrottins er ekki úthlutað.</td>
</tr>
<tr class="odd">
<td><strong>Færslubókarhaus</strong> – Setja upp sjálfgefinn mótlykil fyrir færslubókina sem á að nota sem sjálfgefna færslu í fylgiskjali færslubókarsíðna. Athugaðu að ekki er hægt að tilgreina sjálfgefna mótlykla á færslubókarhaus ef færslubókargerð þeirra er <strong>Komubók</strong> eða <strong>Samþykki</strong>.</td>
<td>Færslubókar færslur í færslubók</td>
<td>Sjálfgefinn mótlykill í færslubók er notaður sem sjálfgefin færsla á síðum fylgiskjals færslubókar.</td>
<td>Notið þennan valkost til að hraða gagnainnfærslu ef flestar færslur í færslubók eru með sama mótlykilinn.</td>
</tr>
</tbody>
</table>





