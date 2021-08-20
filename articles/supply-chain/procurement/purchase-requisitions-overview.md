---
title: Yfirlit yfir „Innkaupabeiðni“
description: Þetta efnisatriði lýsir verkflæði innkaupabeiðna og þeim mismunandi stöðum sem innkaupabeiðni getur verið með.
author: kamaybac
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage, PurchReqConsolidationPartByVendor, PurchReqConsolidationLineDetail, PurchReqConsolidationCreate, PurchReqConsolidationBulkEdit, PurchReqConsolidationAddLine
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2174"
- intro-internal
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08902aa8f7376fb394f319f186a339bb967a871dfa9151eb99b80e89cf797716
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769540"
---
# <a name="purchase-requisition-overview"></a>Yfirlit yfir „Innkaupabeiðni“

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir verkflæði innkaupabeiðna og þeim mismunandi stöðum sem innkaupabeiðni getur verið með.

Eftir því hvernig fyrirtæki þitt er sett upp er hægt að stofna innkaupabeiðnir fyrir vörur sem fyrirtækið notar. Innkaupabeiðni er innra fylgiskjal sem heimila innkaupadeild að kaupa vara eða þjónusta.  

Eftir að innkaupabeiðni hefur verið samþykkt er hægt að nota hana til að stofna innkaupapöntun. Innkaupapantanir eru ytri skjölin sem innkaupadeildin sendir til lánardrottna.

## <a name="creating-purchase-requisitions"></a>Stofna innkaupabeiðnir
Hægt er að stofna innkaupabeiðni á síðunni **Mínar innkaupabeiðnir** og velja vörur og þjónustu sem þarf. Hægt er að velja atriði úr innkaupavörulista sem fyrirtækið hefur búið til, eða þú getur beðið um atriði sem ekki finnast í vörulista með því að velja innkaupategund og slá inn upplýsingar um vöruna.  

Áður en hægt er að senda innkaupabeiðni í endurskoðun verður að stilla verkflæði. Verkflæði er notað til að flytja innkaupabeiðni gegnum endurskoðunarferli, úr á fyrstu stöðu **Drög** í endanlegu stöðuna **Samþykkt**.

### <a name="purchase-requisition-statuses"></a>Stöður innkaupabeiðna

Þegar innkaupapöntun er útbúin er stöðu pöntunar úthlutað á hana. Stöðu er einnig úthlutað á allar línur sem innkaupabeiðni er bætt við. Þegar innkaupabeiðni er send í verkflæði til yfirferðar, eru stöður innkaupabeiðnar og hverrar línu uppfærðar um leið og línurnar færast í gegnum verkflæðisferlið.  

Hægt er að skilgreina verkflæðisferli innkaupabeiðni til að beina innkaupabeiðninni í gegnum yfirferðarferlið sem eitt skjal. Einnig er hugsanlegt að línunum á innkaupabeiðninni verði beint hverri fyrir sig á viðeigandi skoðunaraðila. Þegar innkaupabeiðni er send í verkflæði til yfirferðar, er staða innkaupabeiðnar uppfærð um leið og línan færist í gegnum verkflæðisferlið. Þegar allar línur hafa lokið við endurskoðunarferlið og engin endurskoðunarþrep eru eftir fyrir innkaupabeiðnina er staða heildarinnkaupabeiðninnar uppfærð.

### <a name="purchase-requisition-workflow"></a>Verkflæði fyrir innkaupabeiðni

Eftirfarandi skýringarmynd sýnir stöðurnar sem eru úthlutaðar á innkaupabeiðni og innkaupabeiðnilínu þar sem þau fara gegnum ferlið verkflæði.  

[![Haus og línustöður innkaupabeiðni.](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Vensl hauss og línustöðu innkaupabeiðni

Heildarstaða innkaupabeiðninnar ræðst af stöðu innkaupabeiðnilínanna. Þess vegna verður að ljúka skoðunarferlinu fyrir allar innkaupabeiðnilínur áður en hægt er að ljúka endurskoðunarferlinu fyrir innkaupabeiðnina. Eftirfarandi tafla sýnir stöðurnar sem eru úthlutaðar á innkaupabeiðnihaus og innkaupabeiðnilínu þar sem þau fara gegnum ferlið verkflæði.

<table>
<thead>
<tr class="header">
<th>Staða innkaupabeiðni</th>
<th>Línustaða innkaupabeiðni</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Drög</td>
<td>Drög</td>
<td>Innkaupabeiðni og innkaupabeiðnilínan hafa verið stofnaðar, en þær hafa ekki verið sent til endurskoðunar.&#39; Innkaupabeiðnir og innkaupabeiðnilínur með stöðuna <strong>Drög</strong> er hægt að breyta. Innkaupabeiðni eða innkaupapöntunarlína hefur einnig stöðuna <strong>Drög</strong> ef hún hefur verið afturkölluð en hefur ekki verið send aftur til skoðunar.&#39; <strong>Ábending:</strong> Hægt er að senda eða afturkalla innkaupabeiðni í skjalastigi. Hins vegar er ekki hægt að senda eða afturkalla eina línu innkaupabeiðni.&#39;</td>
</tr>
<tr class="even">
<td>Í skoðun</td>
<td><ul>
<li>Í skoðun</li>
<li>Hafnað</li>
</ul></td>
<td>Ef verkflæðið hefur verið skilgreint til að beina innkaupabeiðnilínum til einstakra yfirlesara getur hver lína haft stöðuna <strong>í yfirferð</strong> eða <strong>Hafnað</strong>. Þegar staða innkaupabeiðni er uppfærð þegar endurskoðunarferli er lokið fyrir allar innkaupabeiðnilínur og engin endurskoðunarferli eru eftir fyrir innkaupabeiðnina.
<ul>
<li><strong>Í yfirferð</strong> – Innkaupabeiðnilínur hafa verið sendar til endurskoðunar. Þegar verkflæðisferlið er lokið fyrir innkaupabeiðnilínu, eftir stöðu línuna <strong>í yfirferð</strong> þar til allar eftirstöðvar innkaupabeiðnilínur hafa verið yfirfarnar.</li>
<li><strong>Hafnað</strong> – Innkaupabeiðnilínu hefur verið hafnað. Hægt er að breyta og endursenda innkaupabeiðnilínur sem er hafnað.</li>
</ul>
Ef innkaupabeiðnilína sem hefur verið hafnað er endursend hefst endurskoðunarferli aftur fyrir allar línur í innkaupabeiðninni sem eru enn í yfirferð. </br><strong>Ábending:</strong> Hægt er að afturkalla innkaupabeiðni sem þegar hefur verið send. Þegar innkaupabeiðni er afturkölluð eru allar aðrar innkaupabeiðnilínur einnig afturkallaðar. Ekki er hægt að eyða innkaupabeiðnilínum sem hafa verið afturkallaðar.</td>
</tr>
<tr class="odd">
<td>Hafnað</td>
<td>Hafnað</td>
<td>Innkaupabeiðni og öllum innkaupabeiðnilínum hefur verið hafnað. Hægt er að endursenda innkaupabeiðnir og innkaupabeiðnilínur sem hefur verið hafnað.</td>
</tr>
<tr class="even">
<td>Samþykkt</td>
<td><ul>
<li>Samþykkt</li>
<li>Hætt við</li>
<li>Lokað</li>
</ul></td>
<td>Allar innkaupabeiðnilínur hafa lokið við endurskoðunarferli og engin endurskoðunarferli eru eftir fyrir innkaupabeiðnina.
<ul>
<li><strong>Samþykkt</strong> – Endurskoðunarferli fyrir línu innkaupabeiðni hefur verið lokið og línan er samþykkt.</li>
<li><strong>Hætt við</strong> – Innkaupabeiðnilína var samþykkt, en hún var afturkölluð þar sem hennar er ekki lengur þörf.&#39; Aðeins er hægt að afturkalla innkaupabeiðnilínur sem hafa verið samþykkiar.</li>
<li><strong>Lokað</strong> – Innkaupabeiðnilínan var samþykkt og skjöl hafa verið mynduð, samkvæmt tilgangi beiðninnar.
<ul>
<li>Ef tilgangur beiðninnar er notkun hefur innkaupapöntun verið mynduð fyrir innkaupabeiðnilínuna.</li>
<li>Ef tilgangur beiðninnar er áfylling hafa eitt eða fleiri uppfyllingarskjöl verið mynduð.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Hætt við</td>
<td>Hætt við</td>
<td>Hætt hefur verið við innkaupabeiðni og allar innkaupabeiðnilínur.</br> <strong>Ábending:</strong> Ef vöru sem er í innkaupabeiðnilínu er ekki lengur þörf, verður að hætta við innkaupabeiðnilínuna ef hún hefur þegar verið samþykkt. Aðeins er hægt að afturkalla innkaupabeiðnilínur sem hafa verið samþykkiar. Ef einhverjar innkaupabeiðnilínur eru í yfirferð mun innkaupabeiðnin hafa stöðuna <strong>í yfirferð</strong>. Í þessu tilfelli er hægt að afturkalla innkaupabeiðnina og eyða viðeigandi innkaupabeiðnilínu.</td>
</tr>
<tr class="even">
<td>Lokað</td>
<td><ul>
<li>Lokað</li>
<li>Hætt við</li>
</ul></td>
<td>Innkaupabeiðnin er lokuð og eitt eða fleiri uppfyllingarskjöl hafa verið mynduð.
<ul>
<li><strong>Lokað</strong> – Innkaupabeiðnilínan var samþykkt og skjöl hafa verið mynduð samkvæmt tilgangi beiðninnar.
<ul>
<li>Ef tilgangur beiðninnar er notkun hefur innkaupapöntun verið mynduð fyrir innkaupabeiðnilínuna.</li>
<li>Ef tilgangur beiðninnar er áfylling hafa eitt eða fleiri uppfyllingarskjöl verið mynduð.</li>
</ul></li>
<li><strong>Hætt við</strong> – Innkaupabeiðnilína var samþykkt, en hún var afturkölluð þar sem hennar er ekki lengur þörf.&#39; Aðeins er hægt að afturkalla innkaupabeiðnilínur sem hafa verið samþykkiar.</li>
</ul>
<strong>Ábending:</strong> Sé er ekki lengur þörf á vöru á línu innkaupabeiðni sem hefur verið lokað, verður að hætta við línu uppfyllingar skjalinu sem var mynduð fyrir línu innkaupabeiðninnar.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Dreifa kostnaði á marga fjárhagslykla
Hægt er að dreifa kostnaði vöru í innkaupabeiðni á marga fjárhagslykla. Ef fyrirtækið notar víddir, eins og deildir og kostnaðarstaði er hægt að dreifa kostnaði afurðar á víddir fyrir fjárhagslega lykla.

## <a name="requisition-purposes"></a>Tilgangur beiðni
Tilgangur beiðni gera ferli uppfyllingar á innkaupabeiðni sveigjanlegri. Þegar beiðni er stofnuð er hægt að úthluta henni tvenns konar málefnum: notkun eða áfyllingu. Það fer eftir tilgangi beiðnar og uppsetningu fyrirtækis hvort eftirspurn beiðna geti verið uppfyllt af innkaupapöntun, flutningspöntun, framleiðslupöntun, eða kanban.  

Í innkaupastefnum er hægt að stjórna málefnum beiðni sem eru tiltæk þegar beiðni er stofnuð fyrir fyrirtækið.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Beiðnir sem hafa notkunartilgang

Innkaupabeiðni sem hefur tilgang notkunar stendur fyrir eftirspurn eftir vörur eða þjónustu sem á að nota innan kerfis af fyrirtækinu. Eftirspurnar sem er stofnuð af þessari gerð innkaupabeiðni uppfylltar alltaf með innkaupapöntun. Ef Supply Chain Management er sjálfvirkt sett upp til að stofna innkaupapantanir, eru innkaupapantanir stofnaðar eftir að innkaupabeiðnin er samþykkt.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Beiðnir sem hafa málefnið áfyllingu

Beiðni með tilganginn áfyllingu stendur fyrir eftirspurn eftir áfyllingu birgða. Notandi gæti til dæmis viljað stofna beiðni um að fylla á vörur svo að hægt sé að selja þær á tilteknum smásölustað á tilteknum tíma. Eftirspurn sem er stofnuð með slíkri beiðni er hægt að uppfylla með innkaupapöntun, flutningspöntun, framleiðslupöntun eða kanban.  

Þegar málefni beiðni er áfylling er eftirspurn er táknuð sem magn en ekki fjárupphæð. Þess vegna eiga reglur um fjárúthlutunarbókhald og fjárhagsáætlunarstýringu, viðskiptareglur fyrir ákvörðun eigna (BRAD), reglur um verk og allar tengdar reglur ekki við. Aðeins afurðir sem eru til í birgðum og og losaðar til tilgreinds lögaðila uppfylla kröfur áfyllingarbeiðni. Til að skilgreina vörurnar sem eru tiltækar þegar málefni beiðni er áfylling skal nota síðuna **Stefnuregla aðgangs fyrir áfyllingu**.  

Til að nota beiðnir með tilganginn áfyllingu verður að setja röðun upp þannig að hún hafi áfyllingarbeiðni með. Uppfyllingaraðferð fyrir eftirspurn sem stofnuð er af slíkri beiðni er síðan ákvörðuð sjálfkrafa, byggt á birgðareglum sem hafa verið settar upp fyrir vörur í fyrirtækinu og áætlaðar með því að nota aðalröðun.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Innkaupabeiðnir og tilboðsbeiðnir
Í sumum tilfellum verður að hefja beiðni um tilboð (BUT) ferli til að auðkenna lánardrottinn og verð fyrir afurðir sem beðið er um í innkaupabeiðni. Hægt er að mynda beiðni um TILBOÐ þegar innkaupabeiðni er í yfirferð. Þegar tilboð er samþykkt, eru upplýsingar um lánardrottinn, verð og svo framvegis, fluttar í innkaupabeiðni.  

Hægt er að setja innkaupabeiðni í bið með því að velja gátreitinn **í bið** á síðunni **upplýsingar um innkaupabeiðni**. Vinnsla innkaupabeiðninnar getur aðeins haldið áfram eftir að taka þær úr bið með því að hreinsa gátreitinn.  

> [!NOTE]
> í e-Procurement, gæti beiðni um tilboð fyrir innkaupabeiðni leyft lánardrottnum að bæta við öðrum línum. Í því tilfelli munu samþykktir varakostir endurspeglast í innkaupabeiðninni.

## <a name="demand-consolidation"></a>Samlegð eftirspurnar
Með sameiningu innkaupabeiðnilína úr mörgum innkaupabeiðnum, er hægt að treysta samningsstöðu sína við lánardrottna ykkar til að ná betri verðlagningu, lægri sendingar- og afgreiðslukostnaði og minni rekstrarkostnað.  

Innkaupabeiðnilínur eru hæfar fyrir sameiningu eftirspurnar ef eftirfarandi yfirlit eru sönn:

-   Innkaupabeiðnin hefur verið samþykkt.
-   Innkaupabeiðnin uppfyllir innkaupa regluskilyrði reglu fyrir handvirka úrvinnslu og eftirspurnar samstæðu.

Samþykktar innkaupabeiðnilínur sem uppfylla skilyrði fyrir handvirka úrvinnslu eru talin upp í **Losa samþykktar innkaupabeiðnir** síðu. Ef lína innkaupabeiðninnar uppfyllir einnig skilyrði fyrir sameiningu eftirspurnar má bæta línunni við í samlegðartækifæri.  

Í samlegðartækifæri er safn innkaupabeiðnilínur sem eru flokkaðar saman þannig innkaupasérfræðingur getur semja bestu viðskiptunum með lánardrottnum. Innkaupabeiðnilínur sem er valið fyrir í samlegðartækifæri birtast á á **samlegð innkaupabeiðni** síðu. Hægt er að breyta línum á þessari síðu ef breytinga er krafist. Einnig er hægt að bæta nýjum línum við eða fjarlægja fyrirliggjandi línur úr samlegðartækifæri.  

Eftir að þú bæta innkaupabeiðnilínum við samlegðartækifæri og gera einhverjar breytingar sem þarf, getur þú stofnað innkaupapöntun fyrir sameinaðar innkaupabeiðnilínur.  

> [!NOTE]
> Breytingar sem gerðar eru á innkaupabeiðnilínu á síðunni **Samlegð innkaupabeiðni** koma fram í innkaupapöntuninni sem er stofnuð. Hins vegar er línan óbreytt í innkaupabeiðninni þannig að saga hennar er varðveitt.  

Til að stofna innkaupabeiðnilínur sem eru ekki hæfar fyrir sameiningu eftirspurnar eða sem eru ekki valdar fyrir sameiningartækifærið verður að vera unnin handvirkt til að stofna innkaupapöntun.

### <a name="consolidating-purchase-requisition-lines"></a>Sameining innkaupabeiðnilína

Ferlið við sameiningu eftirspurnar hefst á tímapunkti þegar innkaupabeiðni hefur verið samþykkt í verkflæði og frátektir fjárhagsáætlunar og verið er að skrá áætlaðar fjárúthlutanir ef fjárhagsáætlunarstýring er skilgreint fyrir þitt fyrirtæki. Eftirfarandi skýringarmynd sýnir vinnsluflæði fyrir sameiningu eftirspurnar.  

[![Flæði ferla fyrir sameiningu eftirspurnar.](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Til að sameina samþykktar innkaupabeiðnilínur, skal fylgja þessum skrefum:

1.  Yfirfara samþykktar innkaupabeiðnilínur sem hefur verið haldið eftir fyrir handvirka úrvinnslu sem eru hæfar fyrir sameiningu eftirspurnar.
2.  Velja innkaupabeiðnilínur til að bæta við samlegðartækifæri.
3.  Stofna ný samlegðartækifæri eða bæta beiðnilínum við fyrirliggjandi samlegðartækifæri.
4.  Gera allar breytingar sem þarf að gera á innkaupabeiðnilínum og fjarlægja línuatriði innkaupabeiðni sem þú vilt ekki lengur að fela í samlegðartækifæri.
5.  Stofna innkaupapantanir fyrir sameinaðar innkaupabeiðnilínur eða innkaup innkaupabeiðnilínur í sameiningu tækifæri.


## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna beiðni um notkun](tasks/create-requisition-consumption.md)

[Verkflæði innkaupabeiðni](purchase-requisitions-workflow.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]