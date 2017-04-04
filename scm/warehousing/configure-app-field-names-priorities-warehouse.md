---
title: "Skilgreina forritið svæðaheiti í Vöruhús forrits"
description: "Þetta efnisatriði lýsir hvernig á að skilgreina og skilgreina heiti forrits vöruhús og forgang Dynamics 365 fyrir Aðgerðir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Skilgreina forritið svæðaheiti í Vöruhús forrits

Þetta efnisatriði lýsir hvernig á að skilgreina og skilgreina heiti forrits vöruhús og forgang Dynamics 365 fyrir Aðgerðir. 

**Athugasemd:** í Þessu efnisatriði eiga aðgerðir í vöruhúsakerfi. Það ekki eiga við um aðgerðir í birgðastjórnun. Dynamics 365 aðgerða - Vöruhús er forrit sem nota má til að framkvæma verkefni vöruhús. Er hægt að skilgreina og skilgreina svæðaheiti eru notuð í forritinu, auk skilgreina forgang sem á að úthluta reitaheiti. Í þessu efnisatriði er útskýrt hvernig tilgreina og skilgreina þessi vöruhús heiti forrits og forgang og hvernig þær eru notaðar í Dynamics 365 aðgerða - Vöruhús. Nákvæmar upplýsingar um hvernig á að skilgreina tengingu við Dynamics 365 aðgerða - Vöruhús, vísa í kennsluefni [setja Upp og skilgreina Dynamics 365 aðgerða - Vöruhús](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Skilgreina vöruhús heiti forrits
===================================

Þegar Dynamics 365 um Aðgerða - Vöruhús í fartæki, er hægt að skilgreina hvernig birta á lýsigögnum í tækið þitt á í **Vöruhúss heiti forrits** síðu. Nýtt fyrirtæki í Dynamics 365 aðgerða, velja **Stofna sjálfgefna uppsetningu** til að mynda öll heiti sem verður notuð í verkflæði fyrir fartæki vöruhúss og úthluta æskilegt ílagshamur og ílagsgerð þeim. Eftir að allar svæðaheiti var mynduð hægt að velja eftirfarandi valkosti inntaks.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valkostur</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Æskilegur ílagshamur</td>
<td>Þessi valkostur ákvarðar hvort scanning svæði eða ílagssvæðið handvirk innfærsla á að sýna fyrir valið svæðisnafn. Þetta er gagnlegt til að aðgreina svæði, allt eftir ef strikamerki eru notuð fyrir svæðið. <strong>Athugasemd:</strong> Fyrir svæðaheiti með æskilegt ílagshamur <strong>Scanning</strong>, er hægt að færa inn upplýsingar handvirkt ef strikamerkið er ólæsilegum eða skemmdar.</td>
</tr>
<tr class="even">
<td>Inntaksgerð</td>
<td>Valkosturinn tilgreinir hvaða gerð inntaks á að nota fyrir valið svæðisnafn. Fjórar valkostir eru tiltækir:
<ul>
<li><strong>Val</strong> - Inniheldur lista yfir valkosti til að velja úr. Reitaheiti við þennan valkost er hægt að breyta.</li>
<li><strong>Dagsetning</strong> - Svæðinu nöfn tilgreint sem dagsetning mun sýna dagsetningu snið með merki. Þetta hjálpar til við að sjá í hvaða snið til að færa inn dagsetningu starfsmanna vöruhússins. Reitaheiti við þennan valkost er hægt að breyta.</li>
<li><strong>Aðgerðakenni</strong> - Ef valið, lyklaborðið tækið verður notað þegar færa inn upplýsingar handvirkt í forritinu. Lyklaborð reynslu er hægt að breyta því hvaða tæki er notað.</li>
<li><strong>Tölulegt</strong> - Fyrir svæðið sem nota tölustafi ílag aðeins nefnir, hægt er að velja þennan valkost til að birta sérsniðna tölur keypad með inntakssvæði en lyklaborð tækis.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Skilgreina vöruhús forritið svæðinu forgang
======================================

Á í **forrits forgang svæði í Vöruhúsi** síðu er hægt að setja svæðaheiti í forgangi mismunandi flokka. Þetta gerir mögulegt að ákveða hvaða upplýsingar eiga að birtast á síðu aðalverkið þegar starfsmenn vöruhúss framkvæmt með því að nota forritið. Ef smellt er á **Stofna sjálfgefna uppsetningu**, sjálfgefna safn flokka forgang verða myndaðir. Mögulegt er að stofna eins margar forgang flokka eftir þörfum, en aðeins þremur flokkum forgang verða sýnd á verk. Það verður að úthluta hvert svæði hlutfallslegt forgang eftir þess flokks forgang þegar Dynamics 365 aðgerða sendir lýsigögn forritið, og mun forritið birta flokka fyrstu þrjá forgang í lýsigagna á verk. Afgangurinn af overflowing lýsigögn verður birt á auka upplýsingar um síðuna. Eftirfarandi tafla sýnir dæmi um fimm forgang flokka.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forgangur flokk</th>
<th>Úthlutuð svæði</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Forgangur 10</td>
<td><ul>
<li>vara</li>
<li>Magn</li>
<li>Mælieining</li>
</ul></td>
</tr>
<tr class="even">
<td> Forgangur 20</td>
<td><ul>
<li>Staðsetning klasa:</li>
<li>Klasi</li>
</ul></td>
</tr>
<tr class="odd">
<td> Forgangur 30</td>
<td><ul>
<li>Vörulýsing</li>
</ul></td>
</tr>
<tr class="even">
<td> Forgangur 40</td>
<td><ul>
<li>Grunnstilling</li>
<li>Litur</li>
<li>Stærð</li>
<li>Stíll</li>
</ul></td>
</tr>
<tr class="odd">
<td> Forgangur 50</td>
<td><ul>
<li>Staður</li>
<li>Númeraplata</li>
</ul></td>
</tr>
</tbody>
</table>

Til dæmis þegar starfsmaður vöruhússins framkvæmir verkefni í farsíma, ef lýsigögn sem verða birtar í forritið samanstendur af eftirfarandi svæðum:

-   vara
-   Magn
-   Mælieining
-   Vörulýsing
-   Stærð og Staðsetningu

Byggt á forgangi forrits-svæði vöruhús sem sett er í töflunni fyrir ofan, eftirfarandi 3 raðir upplýsingar verða birtar á síðu verk:

-   Lína 1: Mælieining Vöru, Magn,
-   Línu 2: Lýsing Vara
-   Lína 3: Stærð

Eftir lýsigögnum, t.d. Staðsetningu verður ekki birt á síðunni verk, en á síðu upplýsingar verða birtar. Frekari upplýsingar og dæmi um notendaviðmótið sjá, vísa til að bóka blog [Announcing Dynamics 365 aðgerða - Vöruhús](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Sjá einnig
--------

[Setja upp og skilgreina Microsoft Dynamics 365 fyrir Aðgerðir-Vöruhús](install-configure-warehousing-app.md)


