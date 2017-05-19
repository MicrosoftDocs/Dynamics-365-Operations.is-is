---
title: "Yfirlit afbrigðalíkön afurðar"
description: "Þessi grein tilgreinir skilmála og hugtök sem tengjast afbrigðalíkönum afurðar. Afbrigðalíkönum afurðar gera notendum kleift að byggja almenna framleiðslubyggingu sem hægt er að nota til að skilgreina margar afurðarafbrigði fyrir eina afurð."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: yuyus
ms.dyn365.intro: Feb-16
ms.dyn365.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 35c3d59abe8c2cb4d2db9fa1cf581f022dbc8c39
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="product-configuration-models-overview"></a>Yfirlit afbrigðalíkön afurðar

[!include[banner](../includes/banner.md)]


Þessi grein tilgreinir skilmála og hugtök sem tengjast afbrigðalíkönum afurðar. Afbrigðalíkönum afurðar gera notendum kleift að byggja almenna framleiðslubyggingu sem hægt er að nota til að skilgreina margar afurðarafbrigði fyrir eina afurð.

Afbrigðalíkön afurða eru stofnuð til að tákna almenna vöruuppbyggingu. Þegar afbrigðalíkan afurðar er sett upp er hægt að búa til einkvæmt afurðarafbrigði sem hefur einkvæma uppskrift og einkvæma leið. Afbrigðalíkönum afurðar nota yfirlýsingarskorður og óskilyrta útreikninga til að meðhöndla vensl og takmarkanir á milli mismunandi afurðarafbrigði. Hægt er að skilgreina afurðir í sölupöntunum, sölutilboðum, innkaupapöntunum og framleiðslupöntunum. Eftirfarandi tafla lýsir skilmálum og hugtökum sem byggja á töfluskorðu.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Íhlutir</td>
<td>Íhlutir eru aðalgrunneiningar afbrigðalíkans afurðar. Íhlutir eru birt í trjáskipulagi í <strong>upplýsingum afbrigðalíkans afurðar sem byggir á Skorðum</strong> síðu. Íhlutir geta innihaldið eftirfarandi hluta:
<ul>
<li>Eigindir</li>
<li>Takmarkanir</li>
<li>Útreikningar</li>
<li>Undiríhlutir</li>
<li>Notendakröfur</li>
<li>Uppskriftarlínur</li>
<li>Leiðaraðgerðir</li>
</ul></td>
</tr>
<tr class="even">
<td>Eigindir</td>
<td>Eigindir lýsa öllum eiginleikum afbrigðalíkans afurðar. Hægt er að nota eigindir til að tilgreina eiginleikana sem hægt er að velja þegar einkvæm afurð er skilgreind. Eigindir eru notaðar í skorðum og skilyrðum. Þegar eigindir eru stofnaðar og þeim bætt við afbrigðalíkan afurðar verður vísað í tengdar eigindagerðir. Hægt er að velja sjálfgildi fyrir eigind. Sjálfgefið gildi er notað í notandaviðmóti skilgreiningar þegar afbrigðalíkan afurðar er skilgreint. Hægt að tilgreina að eigind sé áskilin, ritvarin eða falin.
<ul>
<li><strong>Áskilin </strong> – Velja verður gildi fyrir eigindina þegar varan er skilgreind.</li>
<li><strong>Skrifvarin </strong> – Eigindargildið er birt í skilgreinarlotu, en ekki er hægt að breyta því.</li>
<li><strong>Falið </strong> – Eigindargildið er innifalið í skorðum og skilyrðum, en er ekki birt í skilgreinarlotu.</li>
</ul>
Einnig er hægt að tilgreina skilyrði fyrir eigindir. Ef skilyrðið er uppfyllt verður að færa inn gildi fyrir áskildu eigindina. Skilyrði eru segðir sem þarf að fullnægja fyrir eigindir, uppskriftarlínur og leiðaaðgerðir sem taka á með í afbrigðalíkani afurðar. Allar eigindir sem vísað er til í skilyrði verða áskildar. Ráðlagt er að velja eigind sem áskilda á flipanum <strong>eigindir</strong>. Þetta getur auðveldað að auðkenna áskilda eiginleika. Eigindagildi eru mikilvægur þáttur í endurnýtingu afbrigða. Kerfið notar eigindagildi til að ákvarða hvort til sé skilgreining sem samsvarar valinu sem notandi gerði við skilgreiningarlotu.</td>
</tr>
<tr class="odd">
<td>Gerðir eiginda</td>
<td>Gerðir eiginda tilgreina safn gagnagerða fyrir eigindir sem eru notaðar í afbrigðalíkani afurðar. Eftirfarandi gerðir eiginda eru notaðar:
<ul>
<li><strong>Heiltala</strong> með eða án sviðs</li>
<li><strong>Tugabrot</strong></li>
<li><strong>Texti </strong> með eða án fastlista</li>
<li><strong>Boole-gildi</strong></li>
</ul>
Ef gerð eigindar er <strong>Boole</strong>, <strong>Heiltala</strong> með sviði, eða <strong>Texta</strong> með fastlista , er safn gilda tiltækt þegar afbrigðalíkan afurðar er sett upp. <strong>Ábending:</strong> Leysari furðarafbrigðis viðurkennir aðeins eftirfarandi gerðir eiginda: <strong>Boole</strong>, <strong>Texti</strong> með fastlista og <strong>Heiltala</strong> með sviði. Þess vegna er eingöngu hægt að nota þessar gerðir eiginda í segðarskorður og -skilyrði.</td>
</tr>
<tr class="even">
<td>Takmarkanir</td>
<td>Skorður lýsa takmörkunum á skilgreiningu framleiðslulíkans. Skorður eru notaðar til þess að tryggja að aðeins gild gildi séu valinn þegar afurð er sett upp. Skorður geta annað hvort verið segðarskorður eða töfluskorður:
<ul>
<li>Einungis er hægt að nota segðarskorður fyrir íhlutina sem þær eru bundnar. Segðarskorðurnar fyrir íhlut geta vísað í eigindir undiríhluta íhlutarins. Leysir afurðarafbrigðis er notað til að leysa skorðurnar og þú verður að nota málskipan leysis þegar skorður eru skrifaðar. Fyrir frekari upplýsingar skal skoða efnistengla um segðaskorður og töfluskorður.</li>
<li>Skilgreina verður töfluskorðum áður en hægt er að nota þær á íhlut í afbrigðalíkani afurðar. Töfluskorður geta verið notandaskilgreindar eða kerfisskilgreindar. Notandaskilgreind töfluskorða er gerð fylkis sem má nota til að lýsa samstæðu samsetninga fyrir eigindagildin sem eru skilgreind í eigindagerðum. Ef hátalarar eru t.d. framleidd gæti fylki fyrir notendaskilgreindrar töfluskorðu haft dálka fyrir áferð og grill.</li>
</ul>
<strong>Dæmi</strong> Hátalarar eru tiltækar í fjórum áferðum: Svart, eik, rósarviður og Hvítum. Hátalarar getur haft eina af þremur framgrillum: Svartur, Málmi eða Hvítum. Svart áferð er tiltækur fyrir öll grill en aðrar áferðir takmarkast við tiltekin grill. Eftirfarandi tafla sýnir dæmi um upplýsingar sem birtast í <strong>Leyfðar samsetningar</strong> flipanum á <strong>Breyta töfluskorðu</strong> síðunni.
<table>
<thead>
<tr class="header">
<th>Ljúka cabinet</th>
<th>Framgrill</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Svart</td>
<td>Svart</td>
</tr>
<tr class="even">
<td>Svart</td>
<td>Málmi</td>
</tr>
<tr class="odd">
<td>Svart</td>
<td>Hvítt</td>
</tr>
<tr class="even">
<td>Eik</td>
<td>Svart</td>
</tr>
<tr class="odd">
<td>Rosewood</td>
<td>Hvítt</td>
</tr>
<tr class="even">
<td>Hvítt</td>
<td>Svart</td>
</tr>
<tr class="odd">
<td>Hvítt</td>
<td>Hvítt</td>
</tr>
</tbody>
</table>
Kerfisskilgreind töfluskorða stendur fyrir vörpun á milli gerð eigindar og svæðis í Dynamics 365 for Operations töflu. Kerfisskilgreindrar töfluskorðu tengir gerð eigindar á gagnvirkan hátt við svæðið. Tengillinn virkjar eigind í afbrigðalíkani afurðar til að geta endurspegla gögn í svæði Dynamics 365 for Operations töflu.</td>
</tr>
<tr class="odd">
<td>Útreikningar</td>
<td>Útreikningar tákna viðauka við skorður. Hægt er að nota útreikning til að framkvæma reikniaðgerðir á eigindir af gerðinni <strong>Aukastafa</strong> og <strong>Heiltala</strong> eða rökaðgerðir sem fela í sér eigindir af gerðunum <strong>Texta</strong> með fastlista og <strong>Boole</strong>. Útreikningur hefur markmiðseigind sem mun innihalda niðurstaða segðarútreiknings. Segðarútreikningur er byggður upp með því að nota segðarritil.</td>
</tr>
<tr class="even">
<td>Undiríhlutir</td>
<td>Undiríhlutir endurspegla trjáskipulag afbrigðalíkans afurðar. Hægt er að nota undiríhluti til að smíða uppsetningu afbrigðalíkans afurðar. Undiríhlutir vísa til fyrirliggjandi íhluta. Þess vegna ýtia undiríhlutir undir endurnotkun íhluta í mörgum afbrigðalíkönum afurðar. Á síðunni <strong>upplýsingar uppskriftarlínu</strong> fyrir undiríhlut er hægt að velja sérstakt gildi fyrir undiríhlutinn. Einnig er hægt að velja eigind sem gildið er valið fyrir þegar afbrigðalíkan afurðar er sett upp. Til að taka með afurð sem íhlut eða undiríhlut verður að tilgreina eftirfarandi upplýsingar í síðunni <strong> Stofna afurð</strong> þegar afurð er stofnuð:
<ul>
<li>Í reitnum <strong>Gerð afurðar </strong> skal velja <strong>Vara</strong>.</li>
<li>Í reitnum <strong>undirgerð afurðar </strong> skal velja <strong>afurðarsniðmát</strong>.</li>
<li>Í reitnum <strong>Skilgreiningatækni </strong> skal velja <strong>skorðuskilgreining</strong>.</li>
</ul>
Hægt er að sjá hvort hægt er að nota losaða afurð sem íhlut eða undiríhlut á flipanum <strong>Almennt </strong> á síðunni <strong>upplýsingar um losaðar afurðir</strong>. Ef <strong>skorðuskilgreiningu</strong> er valin í á <strong>skilgreiningartækni</strong> svæðinu er hægt að nota afurðar sem íhlut eða undiríhlut. Hægt er að fela undiríhluti þannig að þeir séu ekki birtir notandanum í skilgreiningarlotu. Eigindir, undiríhlutir og notendakröfur sem tengjast undiríhlutnum eru einnig falin.</td>
</tr>
<tr class="odd">
<td>Notendakröfur</td>
<td>Notendakröfur tákna sértekningu á milli notendaþarfa og tiltekinna íhluti og eiginda. Ekki er hægt að varpa notendaþörfum til vöru. Til dæmis er viðskiptamaður að versla heimabíókerfi. Sölufulltrúinn gæti spurt um stærð herbergisins þar sem viðskiptamaðurinn hyggst setja kerfið upp, til að ákvarða hversu mörg vött eru nauðsynleg. Í þessu dæmi er stærð herbergisins þörf notanda sem hjálpar til við að ákvarða viðeigandi eigindargildi fyrir tiltekna íhluti. Hægt er að fela undiríhluti þannig að þeir séu ekki birtir notandanum í skilgreiningarlotu. Eigindir, undiríhlutir og notendakröfur sem tengjast notendakröfunum eru einnig falin. Hægt er að skrifa skilyrði til að stjórna því hvort notendaþörfin getir verið falin. Þú verður að nota OML-málskipan (Optimization Modeling Language) þegar skorður eru skrifaðar.</td>
</tr>
<tr class="even">
<td>Uppskriftarlínur</td>
<td>Uppskriftarlínur tákna einstök efni íhluta í afbrigðalíkani afurðar. Á <strong>uppskriftarlínuupplýsingar</strong> síðu, eru allar vörur tiltækar til vals. Hægt er að bæta skilyrði við uppskriftarlínuna svo að uppskriftarlínurnar sem eru valdar fyrir einkvæmt afurðarafbrigði geti verið mismunandi, á grundvelli vals notanda þegar vöruskilgreiningarlíkanið er sett upp. Skilyrði eru segðir sem þarf að fullnægja fyrir eigindir, uppskriftarlínur og leiðaaðgerðir sem taka á með í afbrigðalíkani afurðar. Á síðunni <strong>upplýsingar uppskriftarlínu</strong> er hægt að velja sérstakt gildi. Einnig er hægt að varpa eigind sem gildið er valið fyrir þegar afbrigðalíkan afurðar er sett upp.</td>
</tr>
<tr class="odd">
<td>Leiðaraðgerðir</td>
<td>Á síðunni <strong>upplýsingar´ leiðaraðgerðar</strong> er hægt að velja sérstakt gildi. Einnig er hægt að varpa eigind sem gildið er valið fyrir þegar afbrigðalíkan afurðar er sett upp. Skilyrði eru skrifuð líkt og segðarskorður. Skilyrði eru segðir sem þarf að fullnægja fyrir eigindir, uppskriftarlínur og leiðaaðgerðir sem taka á með í afbrigðalíkani afurðar.</td>
</tr>
</tbody>
</table>






