---
title: Stofnun reiknings viðskiptavinar
description: Reikningur viðskiptavinar fyrir sölupöntun er reikningur sem tengist sölunni og sem fyrirtæki gefur viðskiptavini.
author: ShivamPandey-msft
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04c26eec8be61d60908bef67c75958287e7e1a01
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129513"
---
# <a name="create-a-customer-invoice"></a>Stofnun reiknings viðskiptavinar

[!include [banner](../includes/banner.md)]

A **Reikningur viðskiptavinar fyrir sölupöntun** er reikningur sem tengist sölu og stofnun gefur viðskiptavinum. Þessi gerð reikningur viðskiptavinar er stofnaður á grundvelli sölupöntunar, sem felur í sér pöntunarlínur og vörunúmer. Vörunúmer eru tilgreind og bókuð í fjárhaginn. Færslur undirbókar eru ekki tiltæk fyrir reikning viðskiptavinar fyrir sölupöntun. Frekari upplýsingar má sjá í [Stofna sölupöntunarreikninga](tasks/create-sales-order-invoices.md).

A **Ókeypis textareikningur** tengist ekki sölupöntun. Hann inniheldur pöntunarlínur sem fela í sér fjárhagslykla, frjálsar textalýsingar, og söluupphæð sem maður færir inn sjálfur. Ekki er hægt að færa inn vörunúmer á þessa gerð reiknings. Skylda er að færa inn viðeigandi VSK-upplýsingar. Aðallykill fyrir söluna tilgreindur á hverri reikningslínu sem hægt er að dreifa á mörgum fjárhagslykla með því að smella **Dreifingarupphæðir** á síðunni **reikningur með frjálsum texta**. Þar að auki er staða viðskiptavinarins bókuð í safnlykil úr bókunarregla sem notuð er fyrir reikningur með frjálsum texta.

Frekari upplýsingar má finna á

[Búðu til ókeypis textareikninga](../accounts-receivable/create-free-text-invoice-new.md)
[Búðu til ókeypis textareikningssniðmát](../accounts-receivable/create-free-text-invoice-template-new.md)
[Úthlutaðu ókeypis textareikningssniðmáti til viðskiptavinar](tasks/assign-free-text-invoice-template-customer.md)
[Búðu til og birtu endurtekna reikninga með frjálsum texta](tasks/post-recurring-free-text-invoices.md)


A **Pro forma reikningur** er reikningur sem er gerður sem áætlun um raunverulegar reikningsupphæðir áður en reikningurinn er bókaður. Þú getur prentað a **Pro forma reikningur** annaðhvort fyrir reikning viðskiptavinar fyrir sölupöntun eða fyrir frjálsan textareikning. 

>[!NOTE]
> Ef um er að ræða truflun á kerfinu meðan á sölu pro forma reikningsferlinu stendur, getur pro forma reikning verið munaðarlaus. Hægt er að eyða munaðarlausum pro forma reikningi með því að keyra **Eyða pro forma reikningum handvirkt** reglubundið starf. Fara til **Sala og markaðssetning > Reglubundin verkefni > Hreinsun > Eyða pro forma reikningum handvirkt**.

## <a name="using-sales-order-customer-invoice-data-entities"></a>Notkun gagnaeininga sölupöntunar viðskiptavina
Hægt er að nota gagnaeiningar til að flytja inn og flytja út upplýsingar um reikning viðskiptavinar fyrir sölupöntun. Það eru mismunandi einingar fyrir upplýsingarnar á sölureikningshaus og sölureikningslínum.

Eftirfarandi einingar eru tiltækar fyrir upplýsingarnar á haus sölureiknings:

- **Sölureikningabókarhaus** eining (SalesInvoiceJournalHeaderEntity)
- **Sölureikningshausar V2** eining (SalesInvoiceHeaderV2Entity)

Við mælum með að þú notir **Sölureikningabókarhaus** eining, vegna þess að það veitir afkastameiri upplifun fyrir inn- og útflutning söluhausa. Þessi eining inniheldur ekki **Upphæð söluskatts** (INVOICEHEADERTAXAMOUNT) dálkinn, sem táknar virðisaukaskattsvirði á haus sölureiknings. Ef viðskiptaatburðarás þín krefst þessara upplýsinga skaltu nota **Sölureikningshausar V2** aðila til að flytja inn og flytja út upplýsingar um sölureikninghaus.

Eftirfarandi einingar eru tiltækar fyrir upplýsingar um sölureikningslínur:

- **Reikningslínur viðskiptavina** eining (BusinessDocumentSalesInvoiceLineItemEntity)
- **Sölureikningslínur V3** eining (SalesInvoiceLineV3Entity)

Þegar þú ert að ákvarða hvaða línueiningu á að nota fyrir útflutning skaltu íhuga hvort fullur ýtingur eða stigvaxandi ýtingur verði notaður. Að auki skaltu íhuga samsetningu gagna. The **Sölureikningslínur V3** eining styður flóknari atburðarás (til dæmis vörpun á birgðareitina). Það styður einnig útflutningsatburðarás með fullri þrýstingi. Fyrir stigvaxandi ýtir mælum við með að þú notir **Reikningslínur viðskiptavina** aðila. Þessi eining inniheldur mun einfaldari gagnasamsetningu en **Sölureikningslínur V3** eining og er æskilegt, sérstaklega ef ekki er þörf á samþættingu birgðasviðs. Vegna mismunar á kortlagningarstuðningi milli línueininganna, er **Reikningslínur viðskiptavina** eining hefur venjulega hraðari frammistöðu en **Sölureikningslínur V3** aðila.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Bóka og prenta einstaka reikningur viðskiptavinar sem byggðir eru á sölupöntunum
Notið þetta ferli til að stofna reikning sem byggist á sölupöntun. Hægt er að gera þetta ef ákveðið er að reikningsfæra viðskiptamann áður en vörurnar eða þjónustan eru afhent. 

Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu reikningsfærðs magns úr völdum sölupöntunum. Ef bæði magnið **Reikningsafgangur** og magnið **Eftirstöðvar afhendingar** fyrir allar og vörur á sölupöntuninni jafngildir 0 (núlli), breytist staða sölupöntunarinnar í **Reikningsfært**. Ef magn **reikningsafgangs** er ekki núll (0), er staða innkaupapöntunarinnar óbreytt og hægt er að færa inn viðbótarreikninga fyrir hann.

Á listasíðunni **Allar sölupantanir** er hægt að skoða stöðu sölupantana. Nota **Opnir reikningar viðskiptavina** listasíður til að skoða reikningana sem bókaðir voru.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Bóka og prenta einstaka reikningur viðskiptavinar sem byggðir eru á fylgiseðlum og dagsetningunni.
Notaðu þessa aðferð þegar einn eða fleiri fylgiseðlar hafa verið bókaðir fyrir sölupöntun. Reikningur viðskiptamanns er byggður á viðkomandi fylgiseðlum og endurspeglar magnið á þeim. Fjárhagslegar upplýsingar sem koma fram á reikningnum eru byggðar á upplýsingunum sem færðar eru inn þegar reikningurinn er bókaður. 

Hægt er að stofna reikning viðskiptavinar sem er byggður á fylgiseðilslínum sem hafa verið sendar hingað til, jafnvel þótt allar vörur fyrir tiltekna sölupöntun hafi ekki verið sendar. Þetta gæti til dæmis átt við, ef fyrirtækið gefur út einn reikning fyrir viðskiptavin mánaðarlega sem nær yfir allar afhendingar sem sendar eru þann mánuð. Hver fylgiseðill stendur fyrir hlutaafhendingu eða fulla afhendingu á vörum í sölupöntuninni. 

Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu afhents magns úr völdum fylgiseðlum. Ef bæði **Reikningsafgangur** magnið og **Eftirstöðvar afendingar** magnið fyrir allar vörur á sölupöntuninni jafngildir núlli (0), breytist staða sölupöntunarinnar í **Reikningsfært**. Ef magn **reikningsafgangs** er ekki núll (0), er staða innkaupapöntunarinnar óbreytt og hægt er að færa inn viðbótarreikninga fyrir hann. 

Birgðafærslur eru uppfærðar með reikningsnúmeri og staðan í svæðinu **Staða línu** í sölupöntuninni breytist í **Reikningsfært**. 

Skoðaðu stöðu sölupantana á **Allar sölupantanir** listasíðu.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Sameina sölupantanir eða fylgiseðla við bókun
Notið þetta ferli þegar ein eða fleiri sölupantanir eru tilbúnar til bókunar og að sameina á þau í einn reikning. 

Hægt er að velja marga reikninga í á **sölupöntun** listasíða og nota svo **Mynda reikninga** til að sameina þau. Á **Bókun reiknings** síðu er hægt að breyta stillingu fyrir **samantektarröðun** til að draga saman eftir pöntunarnúmeri (þar sem það eru margir fylgiseðlar fyrir eina sölupöntun ) eða eftir reikningslykli (þar sem það eru margar sölupantanir fyrir einn reikningslykil). Nota skal **Skipulag** hnappinn til að sameina sölupantanir í einn reikninga sem byggjast á í stillingar fyrir **samantektarröðun** .

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>Skiptu sölupöntunarreikningum eftir síðu og afhendingarupplýsingum
Þú getur stillt skiptingu reikninga viðskiptavina eftir sölupöntunum eftir síðu eða afhendingarheimilisfangi á **Yfirlitsuppfærsla** flipi á **Færibreytur viðskiptakrafna** síðu. 
 - Veldu **Skipting byggt á reikningssíðu** möguleika á að búa til einn reikning á hverja síðu við færslu. 
 - Veldu **Skipting byggt á upplýsingum um afhendingu reikninga** möguleika á að búa til einn reikning fyrir hverja sölupöntunarlínu afhendingarheimilisfang við bókun. 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>Bóka á tekjureikning fyrir sölupöntunarlínur sem hafa ekkert verð og engan kostnað
Þú munt hafa möguleika á að uppfæra **Tekjur** reikning í **Aðalbók** fyrir sölupöntunarlínur sem hafa ekkert verð og enginn kostnaður. Til að setja upp eða skoða þessar upplýsingar skaltu fara á **Bóka á tekjureikning fyrir núllverð og núllkostnaðar sölupöntunarreikningslínur** breytu á **Fjárhagsbók og söluskattur** flipi á **Færibreytur viðskiptakrafna** síðu. (**Viðskiptakröfur > Uppsetning > Færibreytur viðskiptakrafna**). Veldu **Já** til að uppfæra **Tekjur** gera grein fyrir sölupöntunarreikningslínum sem hafa ekkert verð og engan kostnað. Ef þessi valkostur er valinn mun skírteinið innihalda 0.00 færslur fyrir **Jafnvægi viðskiptavina** og **Tekjur** færslutegundir. Tekjureikningur er skilgreindur á **Birgðafærsla** færibreytusíðu, á **Sölupöntun** reikningsskilgreiningarflipi. Ef þessi valkostur er ekki valinn munu línur sem ekki hafa upplýsingar um verð eða kostnað ekki birtast í **Tekjur** reikning. Í staðinn mun skírteinið innihalda 0,00 færslu fyrir **Jafnvægi viðskiptavina** tegund færslu.

## <a name="line-creation-sequence-number-information"></a>Upplýsingar um raðnúmer línugerðar
Þegar þú bókar reikningslínur viðskiptavina muntu hafa möguleika á að búa til raðnúmer til að búa til línur. Línugerð raðnúmerum er úthlutað meðan á bókunarferlinu stendur. Með því að leyfa óraðnúmeranúmer geturðu hjálpað til við að bæta árangur reikningsbókunar viðskiptavina. Línugerð raðnúmer er hægt að nota með samþættingum þriðja aðila sem búast við rað röð. Hafðu samband við upplýsingatæknideildina þína um allar viðbætur sem gætu samþætt raðnúmerum línugerðar.

Til að setja upp eða skoða þessar upplýsingar, á **Færibreytur viðskiptakrafna** síðu, á **Uppfærslur** flipann, stilltu **Úthlutaðu raðlínunúmerum við bókun á reikningslínum viðskiptavina** valmöguleiki:

- Stilltu valkostinn á **Nei** að nota raðnúmeranúmer fyrir línugerð raðnúmera.
- Stilltu valkostinn á **Já** að nota raðnúmer. Þú verður að stilla valkostinn á **Já** fyrir lögaðila sem hafa aðsetur á Ítalíu. Þú verður líka að stilla það á **Já** ef **CustInvoiceTransRandLineCreationSeqNumFlight** flug er óvirkt.

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
<li><strong>Afhenda nú</strong> – Veljið allt magn sem er fært inn í svæðið <strong>Afhenda nú</strong>. Notaðu þennan valkostur í staðfesta eða afhenda pöntun að hluta til.</li>
<li><strong>Tiltekið</strong> – Velja allt magn sem hafa verið teknar til.</li>
<li><strong>Allt</strong> - Velja allt magn í sölupöntun sem hefur &#39; ekki enn verið uppfært af núverandi gerð skjals.</li>
<li><strong>Fylgiseðill</strong> – Velja allt magn sem hafa verið uppfærðar af fylgiseðli.</li>
<li><strong>Tiltektarmagn og afurðir sem ekki á lager</strong> – Velja allt magn sem hafa verið teknar til og allt magn vöru sem ekki eru í birgðum.&#39;</li>
</ul></td>
</tr>
<tr class="even">
<td>Bókun</td>
<td><ul>
<li>Veljið þennan valkost til að skrá sölupöntun.</li>
<li>Hreinsið þennan valkost til að prenta bráðabirgðaafrit af sölupöntun. <strong>Athugasemd</strong> Ef samningur hefur verið gerður fyrir greiðsluáætlun, mun greiðsluáætlunin ekki verða sýnd á bráðabirgðasölupöntun.&#39; Greiðsluáætlanir verður einungis sýnd á raunverulegu sölupöntuninni.</li>
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
<li><strong>Núverandi</strong> - Prenta skjöl eftir að hver reikningur hefur verið uppfærður.</li>
<li><strong>Eftir</strong> – Prenta skjöl eftir allar reikningur hafa verið uppfærð.</li>
</ul>
<strong>Athugasemd</strong> <strong>Prenta</strong> svæðið býðst aðeins ef valkosturinn <strong>Prenta reikninginn</strong>, <strong>Prenta staðfestingu</strong>, <strong>Prenta tiltektarlista</strong> eða <strong>Prenta fylgiseðla</strong> er valið. Til dæmis, á síðunni <strong>Röðunarsíða skjámynda</strong> hefur þú sett kerfið upp til að raða upplýsingum eftir reikningslykli. Þá er hægt að velja <strong>Eftir</strong> til að prenta skjölin í runu sem er flokkuð af reikningslykli. Annars eru skjöl prentuð áður en vinnslu er lokið og ekki raðað í þá röð sem tilgreint er á síðunni <strong>Flokkunarsíða skjámynda</strong>.&#39;</td>
</tr>
<tr class="even">
<td>Prenta reikning</td>
<td>Veljið þennan valkost til að Prenta reikninginn. Ef þessi valkostur slökkt er hægt að bóka reikning án þess að prenta það.</td>
</tr>
<tr class="odd">
<td>Senda tölvupóst</td>
<td>Veljið þennan valkost til að senda reikninginn fyrir sölupöntun til viðskiptavinar sem tölvupóstsviðhengi eftir að reikningur er bókaður. Viðhengi eru send sem PDF og XML skrár. Þessi valkostur er aðeins tiltækt ef valið er <strong>Virkja CFD (rafrænir reikningar)</strong> valkostinn á síðunni <strong>Færibreytur rafrænna reikninga</strong>. <strong>Athugasemd</strong> (MEX) Þessi stýring er eingöngu tiltæk fyrir lögaðila með aðalaðsetur í Mexíkó.</td>
</tr>
<tr class="even">
<td>Nota ákvörðunarstað prentstýringar</td>
<td>Veljið þennan valkost til að nota prentunarstillingar sem tilgreind eru fyrir færslu, skjali eða kerfiseining á <strong>Prentstjórnunaruppsetning</strong> síðu.</td>
</tr>
<tr class="odd">
<td>Athuga lánamark</td>
<td>Veljið upplýsingar sem verða greindar þegar athugun á lánamarki er framkvæmd.
<ul>
<li><strong>Enginn</strong> – Það er engin krafa um úttektarheimildir.</li>
<li><strong>Staða</strong> – lánamark er athugað gagnvart staða viðskiptamanns.</li>
<li><strong>Staða + fylgiseðill eða innhreyfingarskjal afurða</strong> – lánamark er athugað gagnvart stöðu viðskiptavinar og afhendingar.</li>
<li><strong>Staða + allt</strong> - lánamark er athugað gagnvart staða viðskiptamanns, afhendingar og opnum pöntunum.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditleiðrétting</td>
<td>Veljið þennan valkost til að birta kreditnótu sem debet í fylgiskjali færslna.</td>
</tr>
<tr class="odd">
<td>Kreditfæra eftirstöðvar</td>
<td>Ef verið er að bóka kreditnótu veljið þá þennan valkost til að halda eftirstandandi magni í pöntun.&#39; Ef valmöguleikinn er hreinsaður verða eftirstöðvar settar sem 0 (núll).</td>
</tr>
<tr class="even">
<td>Safnuppfærsla fyrir</td>
<td>Velja hvernig á að taka saman margar sölupantanir:
<ul>
<li><strong>Ekkert</strong> - Ekki &#39; taka saman sölupantanir. Til dæmis verður aðskilinn reikningur stofnaður fyrir hverja sölupöntun.</li>
<li><strong>Reikningslykill</strong> – taka saman öllum völdum pöntunum, samkvæmt skilyrðum sem sett eru upp á síðunni <strong>færibreytur safnuppfærslu</strong>.</li>
<li><strong>Pöntun</strong> – Safna saman völdu sviði pantana í eina tilgreinda pöntun. Pantanir sem er safnað saman, samkvæmt skilyrðum sem sett eru upp á síðunni <strong>færibreytur safnuppfærslu</strong>. Ef þessi valkostur er valinn skal velja gildi í svæðið <strong>sölupöntun</strong>.</li>
<li><strong>Sjálfvirk samantekt</strong> – ef samantektaruppfærslur hafa verið tilgreindar á <strong>safnuppfærslu</strong> síðu, skal safna saman allar valdar pantanir, samkvæmt skilyrðum sem sett eru upp í <strong>færibreytur safnuppfærslu</strong> síðu. Ef safnuppfærsla hefur ekki verið tilgreindur er pöntunin bókuð sér.&#39;</li>
<li><strong>Fylgiseðill</strong> – Safna saman valinni röð af pöntunum í einn reikning á hvern fylgiseðil. Þessi valkostur er bara tiltækur ef <strong>fylgiseðill</strong> er valið í svæðinu <strong>Magn</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
