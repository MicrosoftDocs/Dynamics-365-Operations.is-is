---
title: Intrastat
description: "Þessi grein veitir upplýsingar um intrastat-skýrslur fyrir viðskipti með afurðir, og í sumum tilfellum, með þjónustu á milli landa/svæða innan Evrópusambandsins (ESB). Hún veitir yfirlit yfir ferli skýrslugerðar og lýsir nauðsynlegum stillingum og forsendum."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6d1141d597e95b0d5cabf77c0248697d256b102a
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017


---

# <a name="intrastat"></a>Intrastat

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um intrastat-skýrslur fyrir viðskipti með afurðir, og í sumum tilfellum, með þjónustu á milli landa/svæða innan Evrópusambandsins (ESB). Hún veitir yfirlit yfir ferli skýrslugerðar og lýsir nauðsynlegum stillingum og forsendum.

Intrastat er kerfið sem er notað við öflun upplýsinga og myndun talnagagna um viðskipti með vörur milli landa í Evrópusambandinu (ESB). Intrastat-skýrsla er áskilin þegar afurð fer yfir landamæri annars lands/svæðis innan Evrópusambandsins. Í nokkrum löndum/svæðum eiga Intrastat-skýrslur einnig við um þjónustu. Hægt er að safna skyldu- og valfrjáls einingum í Intrastat-skýrslum. Eftirfarandi einingar eru skylda: virðisaukaskattur (VSK), númer aðilans sem ber ábyrgð á útvegun upplýsinganna, tilvísunartímabil, flæði (komu eða senda), átta stafa vörukóði, samstarfsaðila aðildarríki (aðildarríki vörusendingar á komur) og aðildarríki viðtöku sendingar á, virði varanna, magn vara (nettó margar og fylgivörur einingu) , og eðli færslunnar. Lönd/svæði geta einnig safnað valfrjálsum einingum við ýmis skilyrði. Sumar valfrjálsar einingar eru land/svæði uppruna, afhendingarskilmálar, flutningsmáti, ítarlegri vörukóði en CN8, svæði uppruna sendingar og svæðis viðtöku á komur, vinnslu talnagagna, upplýsingagildi, lýsingu á vörum og tengi/flugvöll fermingar/affermingar.

## <a name="overview-of-the-intrastat-reporting-process"></a>Yfirlit yfir ferli Intrastat-skýrslu
Eftirfarandi kaflar lýsa heildarflæði upplýsinga sem er notað við Intrastat-skýrslu.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Færa inn færslu sem fer yfir landamæri annars lands/svæðis í ESB

Reikningur viðskiptavinar, textareikningur, innkaupareikningur, verkreikningur, fylgiseðill viðskiptavinar, innhreyfingarskjal afurða fyrir lánardrottin eða flutningspöntun er aðeins flutt í Intrastatbókina ef gerð ákvörðunarstaðar lands/svæðis (á sendingar) eða vörusendingu (á aðsent) er **ESB**. Þessi eiginleiki var framlengdur fyrir Microsoft Dynamics 365 for Operations (1611) og gerir kleift að tilgreina aðsetur farmbréfs fyrir viðskipti innan Bandalagsins. Ef aðsetur farmbréfs er ekki það sama og heimilisfang á vinnustað lánardrottins (eða heimilisfang á vinnustað viðskiptavinar fyrir skilapöntun) mun Intrastat-skýrslugerðin nota þessar upplýsingar. Þegar sölupöntun, textareikningur, innkaupapöntun, reikningur lánardrottins, verkreikningur eða flutningspöntun eru stofnuð hafa sumir reitir sem eru tengdir erlendum viðskiptum sjálfgildi í haus skjals eða á línu. Sjálfgefinn færslukóði er fenginn úr samsvarandi reit á síðunni **Færibreytur erlendra viðskipta**. Sjálfgefinn vörukóði, upprunaland /-svæði og upprunaríki/-hérað er sótt frá vöru. Hægt er að breyta sjálfgildum og getur einnig að fylla út í aðrar upplýsingar tengdum erlend viðskiptum: talnagagnasaðferð, flutningsmáta og tengi.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Notaðu Intrastatbókina til að mynda upplýsingar um viðskipti meðal landa/svæða Evrópusambandsins.

Í tölfræðilegum tilgangi eru upplýsingar myndaðar um viðskipti milli ESB landa/svæða í hverjum mánuði. Hægt er að flytja færslur úr textareikningi, reikningi viðskiptavina, fylgiseðli, reikningi lánardrottins, fylgiseðli lánardrottins, verkreikningi eða flutningspöntun, samkvæmt þeim flutningsskilyrðum sem sett eru upp á síðunni **Færibreytur erlendra viðskipta**. Einnig er hægt að færa færslurnar handvirkt inn. Hægt er að uppfæra handvirkt fluttar færslur í intrastatbók, ef uppfærslur eru áskildar. Við sérstök skilyrði sem eru sett upp á síðunni **Þjöppun á intrastat** er hægt að þjappa færslurnar í intrastatbók. Sum lönd/svæði leyfa notkun á þröskuldi lítilla færslna. Síðan er hægt að skrá færslur sem eru undir þeim þröskuldi undir tilgreindum vörukóða. Hægt er að uppfæra vörukóða á samsvarandi línur Intrastatbókar, á grundvelli **Lágmark** stillingar á síðunni **Færibreytur erlendra viðskipta**. Einnig er hægt að þjappa þessar færslur, samkvæmt stillingunni **Þjöppun á intrastat**. Hægt er að sannprófa heilleika færslna í intrastatbókinni, samkvæmt stillingunni **Athuga uppsetningu** á síðunni **Færibreytur erlendra viðskipta**. Gögn í samsvarandi reitum gætu verið sannprófuð fyrir heilleika: land/svæði, ríki eða hérað, þyngd, vörukóði, færslukóði, viðbótar eining, tengi, uppruni, afhending, flutningsaðferð og skattundanþágunúmer. Færslur sem er ekki lokið verða merktar sem ekki gildar.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Notaðu Intrastatbókina til að skrá upplýsingar um viðskipti á meðal landa/svæða Evrópusambandsins

Í tölfræðilegum tilgangi eru upplýsingar skráðar um viðskipti milli ESB landa/svæða í hverjum mánuði. Hægt er að prenta Intrastat-skýrsluna, samkvæmt stillingunni **Vörpun skýrslusniðs** á síðunni **Færibreytur erlendra viðskipta**. Einnig er hægt að prenta rafræna skýrslu, samkvæmt stillingunni **Vörpun skráarsniðs** á síðunni **Færibreytur erlendra viðskipta**. Frekari upplýsingar um Intrastat-skýrslugerð, þar á meðal áskildar forsendur, er að finna í verkskráningum fyrir Intrastat-skýrslur:

-   Mynda ESB Intrastat-skattaskýrslu,
-   Flytja færslur í Intrastat,
-   Tilgreini aðsetur farmbréfs fyrir viðskipti innan Bandalagsins.

## <a name="prerequisites"></a>Forkröfur
Eftirfarandi tafla sýnir frumskilyrði fyrir Intrastat-skýrslur.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Uppsetning aðseturs</td>
<td>Setja upp kóða fyrir land/svæði sem er notað af Alþjóðlegu staðlastofnuninni (ISO).</td>
</tr>
<tr class="even">
<td>Lögaðili</td>
<td>Setja upp skattundanþágunúmer fyrir innflutning/útflutning, numersframlengingu útibús fyrir innflutning/útflutning og intrastat-kóða sem úthlutað er til lögaðila.</td>
</tr>
<tr class="odd">
<td>Stigveldi afurðaflokks (stigveldi sölu, innkaupastigveldi)</td>
<td>Úthluta intrastat-vörukóðum á tegundarhnúta á flipanum <strong>Vörukóðar</strong> á síðunni <strong>Tegundastigveldi</strong>. Þegar þú úthlutar vörukóða á hnút yfirtegundar verður sá kóði notaður á alla hnúta undirtegunda. Valdir vörukóðar verða að vera tiltækir sýninni <strong>Valið</strong> þegar þú velur vörukóða í upplýsingum um losaðar afurðir og á sölupöntun, innkaupapöntun, og flutningspöntunarlínur.</td>
</tr>
<tr class="even">
<td>Upplýsingar um losaðar afurðir</td>
<td>Setja upp eftirfarandi gögn erlendra viðskipta fyrir útgefnar afurðir:
<ul>
<li><strong>Vörukóði</strong> – Veljið annaðhvort lista yfir valdar grunnvörur sem er sótt úr úthlutuðum afurðaflokkum eða fullan lista yfir intrastat-vörukóða.</li>
<li><strong>Tölfræðilegt hlutfall gjalda</strong></li>
<li><strong>Upprunaland /-svæði</strong> – Veljið sjálfgefið land/svæði þar sem vörurnar voru alveg fá eða framleiddar.</li>
<li><strong>Ríki/hérað upprunalands/viðtökustaðar</strong> – Velja sjálfgefið ríki/hérað viðtökustaðar fyrir komur og ríki/hérað fyrir sendingar.</li>
<li><strong>Nettóþyngd í kg</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Viðskiptavinir</td>
<td>Setja upp afhendingaraðsetur viðskiptavinarins í ESB landi/svæði.</td>
</tr>
<tr class="even">
<td>Lánardrottnar</td>
<td>Setja upp afhendingaraðsetur lánardrottins í ESB landi/svæði.</td>
</tr>
<tr class="odd">
<td>Ýmis gjöld</td>
<td>Setja upp ýmsa gjaldakóða til að hafa með í upphæð reiknings, tölfræðilega upphæð eða bæði. Á síðunni <strong>Gjaldakóði</strong> á flipanum <strong>Erlend viðskipti</strong> virkjarðu <strong>Intrastat-reikningsgildi</strong> til að taka með gjaldaupphæð í virði reiknings og virkjar <strong>intrastat-talnagögnum</strong> til að taka með upphæð gjalda í tölfræðilegt gildi.</td>
</tr>
<tr class="even">
<td>Rafræn skýrslugerð</td>
<td>Setja upp grunnstillingar fyrir rafræna skýrslugerð til að flytja út intrastat-gögn í rafræna skrá með sniði sem óskað er eftir af viðeigandi yfirvöldum og til að forskoða intrastat-gögn á notendavænu sniði (til dæmis í Microsoft Excel).</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Uppsetning
Eftirfarandi kaflar lýsa stillingunum sem þarf fyrir Intrastat-skýrslu.

### <a name="set-up-all-required-intrastat-related-lists"></a>Setja upp alla nauðsynlega Intrastat-tengda lista

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Listi</th>
<th>Frekari upplýsingar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vörukóðar</td>
<td>Setja upp tegundastigveldi af gerðinni <strong>Vörukóði</strong> og færið inn allar vörukóða eftir sameinuðum lista yfir vörur. Fyrir hverja vöru eru settar upp eftirfarandi upplýsingar:
<ul>
<li>Færið inn heiti vörunnar og vörukóðann</li>
<li>Stutt nafn og/eða þýtt heiti</li>
<li>Stillingar fyrir skýrslugerð viðbótareininga (fylgivörur) á við flipann <strong>Erlend viðskipti</strong>. Hægt er að velja viðbótareiningar í einingalistanum. Einnig er hægt að tilgreina hvort tilkynna þurfi þyngd grunnvöru til viðbótar við valda einingu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Færslukóðar</td>
<td>Setja upp eðli færslunnar í samræmi við kröfur landsins/svæðiins. Fyrir hvern færslukóða sem er settur upp þarf að setja upp reglur um útreikning reikningsupphæða og upphæðum talnagagna fyrir sölu-/ innkaupapantanir.
<ul>
<li>Fyrir flutningspantanir er sett upp ein eftirfarandi reglum til að reikna upphæðir reiknings og tölfræðiupphæðir:
<ul>
<li><strong>Auð</strong> – upphæð verður að vera 0 (núll).</li>
<li><strong>Fjárhagsleg kostnaðarupphæð</strong> – Upphæðin verður að vera sú sama og fjárhagslegur kostnaður.</li>
<li><strong>Heildarkostnaður</strong> – Upphæðin verður að vera jöfn heildarkostnaði færslunnar.</li>
<li><strong>Handvirk</strong> – Upphæðin verður að vera jöfn og upphæð sem er tilgreind handvirkt í flutningspöntunarlínu.</li>
</ul></li>
<li>Fyrir sölu- og innkaupapantanir er sett upp ein eftirfarandi reglum til að reikna upphæðir reiknings og tölfræðiupphæðir:
<ul>
<li><strong>Auð</strong> – upphæð verður að vera 0 (núll).</li>
<li><strong>Reikningsupphæð</strong> – Upphæðin verður að vera jöfn upphæð sem er reikningsfærð fyrir grunnvöru.</li>
<li><strong>Grunnupphæð</strong> – Upphæðin verður að vera jöfn upphæð sem verður reikningsfærð áður en án afslætti er beitt.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Flutningsaðferðir</td>
<td>Setja upp eðli færslunni í samræmi við kröfur landsins/svæðiins. Fyrir hvern afhendingarmáta er hægt setja upp sjálfgefinn flutningsmáta á flipanum <strong>Erlent</strong>.</td>
</tr>
<tr class="even">
<td>Afh.staður</td>
<td>Setja upp afhendingarstað/flugvöll fermingar/affermingar ef þessum upplýsingum er safnað af landinu/svæðinu.</td>
</tr>
<tr class="odd">
<td>Vinnsla talnagagna</td>
<td>Setja upp vinnslu talnagagna ef þessum upplýsingum er safnað af landinu/svæðinu.</td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Setja upp reglur um þjappanar á Intrastat-færslum

Á síðunni **Þjöppun á intrastat** er hægt að velja reitina sem nota á fyrir þjöppun. Öllum færslum sem hafa sömu samsetningu gilda fyrir valda reiti í intrastatbók verður þjappað saman í eina færslu þegar þjöppunaraðgerð er keyrð í intrastatbók.

### <a name="set-up-foreign-trade-parameters"></a>Setja upp færibreytur erlendra viðskipta

Notaðu síðuna **Færibreytur erlendra viðskipta** til að setja upp færibreyturnar í eftirfarandi töflu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Dálkalykill</th>
<th>Færibreytur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Almennt</td>
<td><ul>
<li><strong>Almennt</strong> – Tilgreindu eftirfarandi upplýsingar:
<ul>
<li>Sjálfgefnir færslukóðar fyrir sölupantanir, innkaupapantanir, kreditnótur og flutningspantanir. Færslukóði sem er settur upp fyrir kreditnótur er einnig notaður sem kóðinn fyrir efnislegar skilavörur og er notaður fyrir frávik í efnislegum skilavörum samanborið við leiðréttingu kreditnótur.</li>
<li>Starfsmaðurinn sem ber ábyrgð á undirbúningi Intrastat-skýrslu.</li>
</ul></li>
<li><strong>Lágmark</strong> – Tilgreindu stillingar fyrir uppfærslu á færslum sem eru fyrir neðan þröskuld:
<ul>
<li>Þröskuldsupphæð og þyngd</li>
<li>Vörukóðinn sem á að nota á færslur sem eru undir þröskuldi</li>
</ul></li>
<li><strong>Flytja</strong> – Tilgreindu skilyrði fyrir flutning á færslum í intrastatbók. Hægt er að tilgreina að færslur eru fluttar þegar vörur uppfylla eitt eða öll eftirfarandi skilyrði:
<ul>
<li>Vörurnar eru ekki þjónustuvörur.</li>
<li>Vörurnar hafa vörukóða.</li>
<li>Vörurnar hafa þyngd.</li>
<li>Vörurnar hafa viðbótareiningar.</li>
</ul></li>
<li><strong>Athuga uppsetningu</strong> – Tilgreindu reglur til að sannprófa heilleika intrastatgagna. Hægt er að velja hvaða gögn eru sannprófuð.</li>
<li><strong>Sléttunarreglur</strong> – Tilgreindu eftirfarandi stillingar til að slétta upphæðir og þyngd í intrastat-skýrslu:
<ul>
<li>Sléttunarreglan (nákvæmni)</li>
<li>Sléttunaraðferð: upp, niður eða venjuleg</li>
<li>Fjöldi aukastafa upphæða og þyngdar</li>
<li>Leiðbeiningar fyrir sléttunarþyngd sem eru minni en 1 kíló (kg): upp að 1 kg, venjuleg eða enga sléttun</li>
</ul></li>
<li><strong>Rafræn skýrslugerð</strong> – Tilgreindu tilvísanir í afbrigði rafrænnar skýrslu, svo að hægt sé að mynda rafræna skrá og skýrslu.</li>
<li><strong>Stigveldi vörukóða</strong> – Tilgreina tegundastigveldi af gerðinni <strong>vörukóða</strong> sem stendur fyrir intrastat-vörukóðann CN8.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tengslaupplýsingar</td>
<td>Tilgreinið nafn á fulltrúa, heimilisfang, skattundanþágunúmerið, símanúmer og faxnúmer.</td>
</tr>
<tr class="odd">
<td>Eiginleikar lands/svæðis</td>
<td>Stilltu land/svæði núgildandi lögaðila á <strong>Innanlands</strong>. Stilla land/svæði ESB-landa/-svæða sem taka þátt í viðskiptum innan ESB með núverandi lögaðila á <strong>ESB</strong>. Fyrir hvert land/svæði skal einnig auðkenna landskóðinn fyrir erlend viðskipti.</td>
</tr>
<tr class="even">
<td>Númeraröð</td>
<td>Tilgreina númeraröð fyrir intrastatbók.</td>
</tr>
</tbody>
</table>

 




