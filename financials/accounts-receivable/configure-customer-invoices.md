---
title: "Stofna reikningur viðskiptavinar."
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fd89921a97782c4d09807a730ab077809304159f
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="create-a-customer-invoice"></a>Stofna reikningur viðskiptavinar.

[!include[banner](../includes/banner.md)]




**Reikningur viðskiptavinar fyrir sölupöntun** er reikningur sem tengist sölunni og sem fyrirtæki gefur viðskiptavini. Þessi gerð reikningur viðskiptavinar er stofnaður á grundvelli sölupöntunar, sem felur í sér pöntunarlínur og vörunúmer. Vörunúmer eru tilgreind og bókuð í fjárhaginn. Færslur undirbókar eru ekki tiltæk fyrir reikning viðskiptavinar fyrir sölupöntun. 

**Reikningur með frjálsum texta** er ekki tengdur sölupöntun. Hann inniheldur pöntunarlínur sem fela í sér fjárhagslykla, frjálsar textalýsingar, og söluupphæð sem maður færir inn sjálfur. Ekki er hægt að færa inn vörunúmer á þessa gerð reiknings. Skylda er að færa inn viðeigandi VSK-upplýsingar. Aðallykill fyrir söluna tilgreindur á hverri reikningslínu sem hægt er að dreifa á mörgum fjárhagslykla með því að smella **Dreifingarupphæðir** á síðunni **reikningur með frjálsum texta**. Þar að auki er staða viðskiptavinarins bókuð í safnlykil úr bókunarregla sem notuð er fyrir reikningur með frjálsum texta.

**Bráðabirgðareikningur** er reikningur sem er útbúinn sem mat á raunverulegu reikningsupphæðinni áður en reikningurinn er bókaður. Hægt er að prenta út bráðabirgðareikning fyrir annað hvort sölureikning eða reikningur með frjálsum texta.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Bóka og prenta einstaka reikningur viðskiptavinar sem byggðir eru á sölupöntunum
Notið þetta ferli til að stofna reikning sem byggist á sölupöntun. Hægt er að gera þetta ef ákveðið er að reikningsfæra viðskiptamann áður en vörurnar eða þjónustan eru afhent. 

Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu reikningsfærðs magns úr völdum sölupöntunum. Ef bæði magnið **Reikningsafgangur** og magnið **Eftirstöðvar afhendingar** fyrir allar og vörur á sölupöntuninni jafngildir 0 (núlli), breytist staða sölupöntunarinnar í **Reikningsfært**. Ef magn **reikningsafgangs** er ekki núll (0), er staða innkaupapöntunarinnar óbreytt og hægt er að færa inn viðbótarreikninga fyrir hann.

Á listasíðunni **Allar sölupantanir** er hægt að skoða stöðu sölupantana. Nota **Opnir reikningar viðskiptavina** listasíður til að skoða reikningana sem bókaðir voru.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Bóka og prenta einstaka reikningur viðskiptavinar sem byggðir eru á fylgiseðlum og dagsetningunni.
Notaðu þessa aðferð þegar einn eða fleiri fylgiseðlar hafa verið bókaðir fyrir sölupöntun. Reikningur viðskiptamanns er byggður á viðkomandi fylgiseðlum og endurspeglar magnið á þeim. Fjárhagslegar upplýsingar sem koma fram á reikningnum eru byggðar á upplýsingunum sem færðar eru inn þegar reikningurinn er bókaður. 

Hægt er að stofna reikningur viðskiptavinar út frá línuvörum fylgiseðils sem sendar hafa verið fram að þessu, jafnvel þótt allar vörur tiltekinnar sölupöntunar hafi ekki verið sendar ennþá. Þetta gæti til dæmis átt við, ef fyrirtækið gefur út einn reikning fyrir viðskiptavin mánaðarlega sem nær yfir allar afhendingar sem sendar eru þann mánuð. Hver fylgiseðill stendur fyrir hlutaafhendingu eða fulla afhendingu á vörum í sölupöntuninni. 

Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu afhents magns úr völdum fylgiseðlum. Ef bæði **Reikningsafgangur** magnið og **Eftirstöðvar afendingar** magnið fyrir allar vörur á sölupöntuninni jafngildir núlli (0), breytist staða sölupöntunarinnar í  **Reikningsfært**. Ef magn **reikningsafgangs** er ekki núll (0), er staða innkaupapöntunarinnar óbreytt og hægt er að færa inn viðbótarreikninga fyrir hann. 

Birgðafærslur eru uppfærðar með reikningsnúmeri og staðan í svæðinu **Staða línu** í sölupöntuninni breytist í **Reikningsfært**. 

Á listasíðunni **Allar sölupantanir** er hægt að skoða stöðu sölupantana.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Sameina sölupantanir eða fylgiseðla við bókun
Notið þetta ferli þegar ein eða fleiri sölupantanir eru tilbúnar til bókunar og að sameina á þau í einn reikning. 

Hægt er að velja marga reikninga í á **sölupöntun** listasíða og nota svo **Mynda reikninga** til að sameina þau. Á **Bókun reiknings** síðu er hægt að breyta stillingu fyrir **samantektarröðun** til að draga saman eftir pöntunarnúmeri (þar sem það eru margir fylgiseðlar fyrir eina sölupöntun ) eða eftir reikningslykli (þar sem það eru margar sölupantanir fyrir einn reikningslykil). Nota skal **Skipulag** hnappinn til að sameina sölupantanir í einn reikninga sem byggjast á í stillingar fyrir **samantektarröðun** .

## <a name="additional-settings-that-change-the-posting-behavior"></a>Frekari stillingar sem breyta bókununarhegðun
Eftirfarandi svæði breyta hegðun bókunarferlanna.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Reitur</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Magn</td>
<td>Velja magnið sem á að byggja bókun skjalsins á. Valkostirnir sem eru tiltækir eru breytilegir, eftir gerð skjals sem verið er að bóka, eins og fylgiseðil eða reikning.
<ul>
<li><strong>Afhenda nú </strong> – Veljið allt magn sem er fært inn í svæðið <strong>Afhenda nú</strong>. Notaðu þennan valkostur í staðfesta eða afhenda pöntun að hluta til.</li>
<li><strong>Tiltekið</strong> – Velja allt magn sem hafa verið teknar til.</li>
<li><strong>Allt </strong>- veldu allt magn á sölupöntun sem þú hefur ekki enn uppfært af núverandi gerð skjals</li>
<li><strong>Fylgiseðill </strong> – Velja allt magn sem hafa verið uppfærðar af fylgiseðli.</li>
<li><strong>Tiltektarmagn og afurðir sem ekki á lager </strong> – Velja allt magn sem hafa verið teknar til og allt magn vöru sem ekki eru í birgðum.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bókun</td>
<td><ul>
<li>Veljið þennan valkost til að skrá sölupöntun.</li>
<li>Hreinsið þennan valkost til að prenta bráðabirgðaafrit af sölupöntun. <strong>Athugasemd</strong> Ef samningur hefur verið gerður fyrir greiðsluáætlun, mun greiðsluáætlunin ekki verða sýnd á bráðabirgðasölupöntun. Greiðsluáætlanir verður einungis sýnd á raunverulegu sölupöntuninni.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Valið síðar</td>
<td>Velja þennan valkost til að nota völdu fyrirspurnina síðar. Þessi valkostur er notaður fyrir runuvinnslu. Fyrirspurnin er keyrð þegar runuvinnsla er keyrð.</td>
</tr>
<tr class="even">
<td>Minnka magn</td>
<td>Veljið þennan valkost til að minnka sjálfvirkt afhent magn þegar skjalið er bókuð, þannig að afhent magn jafngildi tiltækar birgðir.</td>
</tr>
<tr class="odd">
<td>Prenta</td>
<td>Velja hvenær á að prenta skjöl.
<ul>
<li><strong>Núverandi </strong> - Prenta skjöl eftir að hver reikningur hefur verið uppfærður.</li>
<li><strong>Eftir </strong> – Prenta skjöl eftir allar reikningur hafa verið uppfærð.</li>
</ul>
<strong>Athugasemd</strong> <strong>Prenta </strong> svæðið býðst aðeins ef valkosturinn <strong>Prenta reikninginn</strong>, <strong>Prenta staðfestingu</strong>, <strong>Prenta tiltektarlista </strong> eða <strong>Prenta fylgiseðla </strong> er valið. Til dæmis, á síðunni <strong>Röðunarsíða skjámynda </strong> hefur þú sett kerfið upp til að raða upplýsingum eftir reikningslykli. Þá er hægt að velja <strong>Eftir </strong> til að prenta skjölin í runu sem er flokkuð af reikningslykli. Annars eru skjöl prentuð áður en vinnslu er lokið og ekki raðað í þá röð sem tilgreint er á síðunni <strong>Flokkunarsíða skjámynda</strong>.</td>
</tr>
<tr class="even">
<td>Prenta reikning</td>
<td>Veljið þennan valkost til að Prenta reikninginn. Ef þessi valkostur slökkt er hægt að bóka reikning án þess að prenta það.</td>
</tr>
<tr class="odd">
<td>Senda tölvupóst</td>
<td>Veljið þennan valkost til að senda reikninginn fyrir sölupöntun til viðskiptavinar sem tölvupóstsviðhengi eftir að reikningur er bókaður. Viðhengi eru send sem PDF og XML skrár. Þessi valkostur er aðeins tiltækt ef valið er <strong>Virkja CFD (rafrænir reikningar)</strong> valkostinn á síðunni <strong>Færibreytur rafrænna reikninga </strong>. <strong>Athugasemd</strong> (MEX) Þessi stýring er eingöngu tiltæk fyrir lögaðila með aðalaðsetur í Mexíkó.</td>
</tr>
<tr class="even">
<td>Nota ákvörðunarstað prentstýringar</td>
<td>Veljið þennan valkost til að nota prentunarstillingar sem tilgreind eru fyrir færslu, skjali eða kerfiseining á <strong>Prentstjórnunaruppsetning</strong> síðu.</td>
</tr>
<tr class="odd">
<td>Athuga lánamark</td>
<td>Veljið upplýsingar sem verða greindar þegar athugun á lánamarki er framkvæmd.
<ul>
<li><strong>Ekkert </strong> – Engin krafa um athugun á lánamarki.</li>
<li><strong>Staða </strong> – lánamark er athugað gagnvart staða viðskiptamanns.</li>
<li><strong> Staða + fylgiseðill eða innhreyfingarskjal afurða </strong> – lánamark er athugað gagnvart stöðu viðskiptavinar og afhendingar.</li>
<li><strong>Staða + allt </strong> - lánamark er athugað gagnvart staða viðskiptamanns, afhendingar og opnum pöntunum.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditleiðrétting</td>
<td>Veljið þennan valkost til að birta kreditnótu sem debet í fylgiskjali færslna.</td>
</tr>
<tr class="odd">
<td>Kreditfæra eftirstöðvar</td>
<td>Ef verið er að bóka kreditnótu veljið þá þennan valkost til að halda eftirstandandi magni í pöntun. Ef valmöguleikinn er hreinsaður verða eftirstöðvar settar sem 0 (núll).</td>
</tr>
<tr class="even">
<td>Safnuppfærsla fyrir</td>
<td>Velja hvernig á að taka saman margar sölupantanir:
<ul>
<li><strong>Ekkert</strong> – Ekki taka saman sölupöntunum. Til dæmis verður aðskilinn reikningur stofnaður fyrir hverja sölupöntun.</li>
<li><strong>Reikningslykill</strong> – taka saman öllum völdum pöntunum, samkvæmt skilyrðum sem sett eru upp á síðunni <strong>færibreytur safnuppfærslu</strong>.</li>
<li><strong>Pöntun</strong> – Safna saman völdu sviði pantana í eina tilgreinda pöntun. Pantanir sem er safnað saman, samkvæmt skilyrðum sem sett eru upp á síðunni <strong>færibreytur safnuppfærslu </strong>. Ef þessi valkostur er valinn skal velja gildi í svæðið <strong>sölupöntun</strong>.</li>
<li><strong>Sjálfvirk samantekt </strong> – ef samantektaruppfærslur hafa verið tilgreindar á <strong>safnuppfærslu</strong> síðu, skal safna saman allar valdar pantanir, samkvæmt skilyrðum sem sett eru upp í <strong>færibreytur safnuppfærslu</strong> síðu. Ef safnuppfærsla hefur ekki verið tilgreindur er pöntunin bókuð sér.</li>
<li><strong>Fylgiseðill</strong> – Safna saman valinni röð af pöntunum í einn reikning á hvern fylgiseðil. Þessi valkostur er bara tiltækur ef <strong>fylgiseðill</strong> er valið í svæðinu <strong>Magn</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>






