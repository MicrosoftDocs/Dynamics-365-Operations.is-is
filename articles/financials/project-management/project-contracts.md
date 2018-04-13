---
title: Verksamningar
description: "Þetta efnisatriði gefur dæmi um verksamninga sem hægt er að búa til fyrir ýmsar gerðir verka og uppruna fjármögnunar og hvernig hægt er að vinna með samninga og senda viðskiptavinum reikninga vegna verka í Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e46393b9ac8797bf12cca12099d177980b75ba38
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="project-contracts"></a>Verksamningar

[!INCLUDE [banner](../includes/banner.md)]

Þessi grein gefur dæmi um verksamninga sem hægt er að búa til fyrir ýmsar gerðir verka og uppruna fjármögnunar og hvernig hægt er að vinna með samninga og senda viðskiptavinum reikninga vegna verka í Microsoft Dynamics 365 for Finance and Operations.

Gerð verks sem er stofnuð fyrir verksamningur ákvarðar aðferðina sem er notuð til að reikningsfæra viðskiptavini verksins. Hægt er að breyta verksamningi og tengdum verkum, en ekki er hægt að breyta gerð verks. 

Með því að nota verksamning er hægt að reikningsfæra eitt eða fleiri verk samtímis. Verksamningurinn stuðlar einnig að því að tryggja að samræmt reikningsfærsluferli sé notað fyrir hvert undirverk verkskipulags. 

Hvert verk sem verður reikningsfært verður að tengja við verksamning. Stillingar fyrir verksamning eiga við öll verk og undirverk sem tengjast verksamningnum. 

Verksamningur getur tilgreint fleiri en einn uppruna fjármögnunar. Þannig er hægt að skipta reikningagerð á marga fjármögnunaraðila, setja upp fjármögnunartakmörk þannig að uppruni fjármögnunar eru ekki rukkaðir um meira en tilgreinda upphæð, og stilla fjármögnunarreglur til að gjaldfæra útgjöld.

## <a name="funding-for-project-contracts"></a>Fjármögnun fyrir verksamninga
Sumar verksamninga tilgreina að margir aðila deila ábyrgð fyrir fjármögnunar verkkostnaðar. Hér eru nokkur dæmi:

-   Stór viðskiptavinar sem er með margar deildir biður um að fjármögnun verks sé skipt eftir deild.
-   Fyrirtækið þitt deilir kostnaði fyrir stórt verk með ytri fyrirtæki.
-   Vegavinnuverk er samfjármagnað af tveimur sveitarfélaga.
-   Á Brúarvinnuverk er fjármagnað af opinber styrkur og einkafyrirtæki.

Í Finance and Operations er hægt að skipta reikningum fyrir einstaka færslu eða allt verkið á milli margra viðskiptavina, styrkja eða fyrirtækja. 

Í verkum sem hafa mörg fjármögnunaraðila, verða allir aðilar sem eiga þátt í fjármögnunar ítarlega fjármögnunarverks kallast fjármögnunaraðilar. Eftir að viðskiptavini, fyrirtæki eða styrks er skilgreind sem fjármögnunaraðilar, má úthluta þeim á ein eða fleiri fjármögnunarreglur. Fjármögnunarreglur innihalda þau skilyrði sem ákvarða hvernig gjöldum er úthlutað á ýmsar fjármögnunaraðila fyrir verk. 

Þar sem vörur í birgðum, eins og þær sem birtast á innkaupabeiðnir og innkaupapantanir, er ekki hægt að skipta, ekki er hægt að skipta, er ekki hægt að skipta kostnaðarupphæð milli marga fjármögnunaraðila á tíma dreifingarinnar. Þess vegna helst upprunagildi fjármögnunar 0 (núll) þar til úthreyfing birgða er bókuð. Þegar bókað er úthreyfing birgða, kostnaðarupphæð er dreift samkvæmt reglum um dreifingu á reikninga fyrir verkið.

Hér eru nokkur skref sem má grípa til svo auðveldara sé að skipta reikningum á milli marga fjármögnunaraðila:

-   Tilgreinið að allar færslur sem eru færðar inn fyrir verk nota sama sölugjaldmiðill og verksamning.
-   Setja upp fjármögnunarmörk, þannig að á fjármögnunaraðila er ekki reikningsfærður fyrir meira en tilgreind upphæð hvað varðar verk.
-   Skilgreina fjármögnunarreglur og hámarki fjármögnunar fyrir hvern starfsmann, vöru, tegund, tegundaflokk og færslugerð (eða fyrir allar færslugerðir).
-   Veljið valfrjálsar upphafs- og lokadagsetningar til að skilgreina tímabil þegar hver fjármögnunarregla er gild.
-   Tilgreinið þá prósentu sem hver fjármögnunaraðila er ábyrgur fyrir.
-   Tilgreina hvaða fjármögnunaraðila er ábyrgur fyrir sléttunarmismunur sem eru orsökuð af útreikninga á úthlutun fjármögnunar.
-   Setja upp reglur sem ákvarða hvernig verkkostnað eru reikningsfærð til utanaðkomandi viðskiptavina og gjaldfærð fyrir samstæðufyrirtæki.
-   Skrá á færslur fyrir fjármögnunarlykil í biðstöðu þar til viðbótarfjármagn fæst eða þar til notandi ákveður að bera kostnaðinn innan fyrirtækis.

Til að ákvarða hvaða skattflokk til að tengja við færslu, er leitað í verkinu fyrir úthlutun í skattflokk. Ef enginn úthlutunin skattflokks er gerð á verkstiginu, er leitað í verksamning.

### <a name="example-multiple-funding-sources-simple"></a>Dæmi: marga uppruni fjármögnunar (einfalt)

Eftirfarandi tafla gefur dæmi fyrir stjórnun úthlutunar á fjármögnun milli marga uppruna fjármögnunar. Þessar aðstæður eru byggð á eftirtöldum ályktunum:

-   Forgangsstillingar eru látnar vera þáttur í úthlutun fjármagns áður en önnur skilyrði fjármögnunarreglu er beitt.
-   Engin dagsetningabil hefur verið tilgreindur til að skilgreina tímabil þegar fjármögnunarreglan er í gildi.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Aðstæður</strong></td>
<td><strong>Uppruni fjármögnunar </strong></td>
<td><strong>Úthlutunarhlutfall </strong></td>
<td><strong>Úthlutanaforgangur</strong></td>
</tr>
<tr class="even">
<td>Þú vilt úthluta kostnaði til einn uppruni fjármögnunar þar til fjármagn eru uppurið, úthluta kostnaði til annars uppruni fjármögnunar þar til fjármagn þess er uppurið, og úthluta að lokum eftirstandandi kostnaður á þriðja uppruni fjármögnunar.</td>
<td><ul>
<li>Uppruni fjármögnunar　1</li>
<li>Uppruni fjármögnunar　2</li>
<li>Uppruni fjármögnunar　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Þú vilt úthluta 75 prósent af kostnaði í einn uppruna fjármögnunar og 25 prósent í annan uppruna fjármögnunar. Þegar annað hvor uppruni fjármögnunar er uppurinn viltu greiða eftirstandandi kostnað frá þriðja uppruna fjármögnunar.</td>
<td><ul>
<li>Uppruni fjármögnunar　1</li>
<li>Uppruni fjármögnunar　2</li>
<li>Uppruni fjármögnunar　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Þú vilt úthluta 75 prósent af kostnaði í einn uppruna fjármögnunar og 25 prósent í annan uppruna fjármögnunar. Þegar annað hvor uppruni fjármögnunar er uppurinn viltu skipta eftirstandandi kostnaður á milli þriðja uppruni fjármögnunar og fjórða uppruni fjármögnunar.</td>
<td><ul>
<li>Uppruni fjármögnunar　1</li>
<li>Uppruni fjármögnunar　2</li>
<li>Uppruni fjármögnunar　3</li>
<li>Uppruni fjármögnunar　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Þú vilt úthluta fyrstu 25 prósent af kostnaði í einn uppruni fjármögnunar og afganginum á seinni uppruni fjármögnunar.</td>
<td><ul>
<li>Uppruni fjármögnunar　1</li>
<li>Uppruni fjármögnunar　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Dæmi: marga uppruni fjármögnunar (flókið)

Þú ert með þrjá uppruna fjármögnunar sem þú vilt nota í eftirfarandi röð:

1.  Notið uppruni fjármögnunar 2 og uppruni fjármögnunar 3 jafnt þar til uppruni fjármögnunar 2 er uppurinn.
2.  Halda áfram að nota uppruni fjármögnunar 3 þar til hún er uppurinn.
3.  Notið uppruni fjármögnunar 1 þar til uppruni fjármögnunar 3 er uppurinn.

Til að ná þessu markmiði þarf að gera eftirfarandi:

-   Setja upp hámark fjármögnunar fyrir uppruni fjármögnunar 2 og 3, fyrir viðeigandi upphæðir.
-   Stofna eftirfarandi fjármögnunarreglur:
    -   Regla 1 (Forgangur 1): Úthluta 50 prósent færsla í uppruni fjármögnunar 2 og 50 prósent í uppruni fjármögnunar 3.
    -   Regla 2 (Forgangur 2): Úthluta 100 prósent færsla í uppruni fjármögnunar 3.
    -   Regla 3 (Forgangur 3): Úthluta 100 prósent færsla í uppruni fjármögnunar 1.

Þessi uppsetning virkar þar sem færslur eru athugaðar gagnvart reglur og mörk til að ákvarða hvort einhver þeirra eigi við færsluna. Ef engar sérstakar reglur eða takmarkanir eiga við um færsluna, gilda allar færslureglur. Allar færslureglur samsvara allar færslur. 

Ef regla finnst sem samsvarar færslu, er prósentu sem hefur verið úthlutað í þeirri reglu beitt fyrst, en aðeins eftir samsvaranir eru athugaðar gagnar öllum mörkum sem hafa verið settar upp. Ef mörk hafi verið náð og fjármagn uppruni fjármögnunar eru uppurin, er fjármögnunarreglan sem er tengdur við hámark fjármögnunar hunsuð og forritið athugar næsta regluna sem á við. 

Í sumum tilvikum, aðeins hluti af færslu er hægt að úthluta samkvæmt reglu. Þetta gæti gerst þar sem mörk er náð þegar færsluna er úthlutað. Í þessu tilfelli eru aðeins tiltekna upphæð úthlutað samkvæmt þeirri reglu, eins og 50 prósent á hvern uppruni fjármögnunar. Þetta er tilfellið í reglu 1, sem er lýst fyrr í þessum hluta. Afgangurinn er úthlutað samkvæmt næstu reglu í röðinni. 

Eftirfarandi tafla athugar þessar aðstæður í meiri smáatriðum.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Áhersla</strong></td>
<td><strong>Upplýsingar</strong></td>
</tr>
<tr class="even">
<td>Fjármögnunarreglur</td>
<td><ul>
<li>Regla 1 (Forgangur 1): Allar færslur. Úthluta uppruni fjármögnunar 2 við 50% og uppruni fjármögnunar 3 við 50%.</li>
<li>Regla 2 (Forgangur 2): Allar færslur. Úthluta uppruna fjármögnunar 3 á 100%.</li>
<li>Regla 3 (Forgangur 2): Allar færslur. Úthluta uppruna fjármögnunar 1 á 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Fjármögnunarmörk</td>
<td><ul>
<li>Uppruni fjármögnunar 1 takmörk = 10.000,00</li>
<li>Uppruni fjármögnunar 2 takmörk = 500,00</li>
<li>Uppruni fjármögnunar 3 takmörk = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Færsla 1</td>
<td><strong>Færsluupphæð:</strong> 100,00<strong>fjármögnun:</strong> Færslan er greitt samkvæmt reglu 1 eingöngu, þar sem færslan er fullgreidd eftir að reglu 1 er beitt. Færslan er fjármagnað jafnt milli uppruni fjármögnunar 2 og uppruni fjármögnunar 3 .
<ul>
<li>Uppruni fjármögnunar 2: 50,00</li>
<li>Uppruni fjármögnunar 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Færsla 2</td>
<td><strong>Færsluupphæð:</strong> 5.000,00<strong>Fjármögnun:</strong> Færslan er greidd í samræmi við allar þrjár reglunar. <strong>Regla 1</strong>
<ul>
<li>Uppruni fjármögnunar 2: 450,00</li>
<li>Uppruni fjármögnunar 3: 450,00</li>
</ul>
<strong>Regla 2</strong>
<ul>
<li>Uppruni fjármögnunar 3: 250.00 (= 750.00 – 50.00 – 450.00)</li>
</ul>
<strong>Regla 3</strong>
<ul>
<li>Uppruni fjármögnunar 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Samtals fjármagn sem er dreift á hvern uppruni fjármögnunar</td>
<td><ul>
<li>Uppruni fjármögnunar 1: 3.850,00</li>
<li>Uppruni fjármögnunar 2: 500,00</li>
<li>Uppruni fjármögnunar 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Innheimtureglur
Þegar verksamningur er saminn við viðskiptavin skilgreinirðu hvernig og hvenær hægt er að reikningsfæra á viðskiptavininn fyrir vinnu við verk. Eftir að þú setur upp verksamninginn og verkið, geturðu sett upp reikningsreglur fyrir verk. Reikningsreglur byggist á skilmálum verks sem er tilgreindur í verksamningnum. Reikningsreglur sem hægt er að stofna velta á skilmálum í verksamningi og tegund verks, eins og Tími og efni eða Fast verð, sem tengt er við reikningsreglu. Hægt er að stofna fleiri en eina reikningsreglu fyrir verksamning. Einnig er hægt að úthluta reikningsreglu á mörg verk sem tengjast sama verksamning og hafa svipaðar innheimtuskilmála. 

Þú getur sett upp eftirfarandi gerðir innheimtureglna:

-   **Afhendingareining** - Stofna reikning viðskiptavinar þegar þú hefur lokið einingu afhendingar. Skilgreina einingarnar afhendingar í samningnum.
-   **Framvinda** - Sendu viðskiptavini reikning þegar þú klárar ákveðið hlutfall af verkefninu. Þú getur sett upp innheimtureglu til að sjálfkrafa reikna hlutfall lokinnar vinnu, eða þú getur handvirkt reiknað hlutfall af lokinni vinnu og fjárhæð sem á að reikningsfæra viðskiptavininn.
-   **Þáttaskil**– Stofna reikning fyrir alla upphæð áfanga þegar nýjum verkáfanga er náð.
-   **Gjald** - Sendu viðskiptavini reikning fyrir þjónustu þína auk umsýsluþóknun, venjulega hlutfall af kostnaði við þjónustu.
-   **Tími og efni** - Stofna reikning viðskiptavinar fyrir verðmæti tíma og efnum sem notuð eru á verkefninu.

Fyrir allar gerðir reikningsreglum, er hægt að tilgreina hlutfall varðveislu að draga úr reikningi viðskiptavinar þar til verki nær á samþykkt við stig. Hlutfall varðveislu á greiðslu er tilgreindur í verksamningnum. Upphæðin er reiknuð út á grunni, og dreginn frá, heildarvirði lína í reikningi viðskiptavinar. 

Fyrir **Tími og efni** og **Framvindu** reikningsreglur, geturðu úthlutað gjaldfæranlegum flokkum. Reikningshæfar tegundir tilgreina færslur sem eiga að birtast í reikningum viðskiptavina. 

Þegar þú ert tilbúinn til að reikningsfæra viðskiptavininn, er fjárhæð sem á að reikningsfæra fyrir verkefnið reiknuð út á grunni innheimtureglna og reikningstillaga er mynduð. 

Eftirfarandi kaflar gefa dæmi sem sýna hvernig á að setja upp og stjórna reikningsreglu fyrir verk.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Dæmi: Stofna reikningsreglur byggt á fjölda afhentra eininga

Fyrirtækið þitt fellst á að nota þjónustuna í samtals fimm þjálfunarsetur fyrir starfsmann viðskiptavinar á kostnaðinum 10.000 fyrir hverja þjálfunarsetu. Að reikningsfæra á viðskiptavininn eftir hverja þjálfun setu. 

Þegar þú gerir Uppsetning reikningsreglna fyrir verksamning notarðu eftirfarandi gildum:

-   Eining afhendingartíma er eina þjálfun setu.
-   Einingarverð er 10.000 á þjálfun setu.
-   Fjöldi eininga sem er fimm þjálfun lotur.

Þegar þú lýkur einni þjálfunarlotu, geturðu stofnað reikning fyrir 10.000 fyrir fyrsta afhentu vörurnar og sendir reikning til viðskiptavinar.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Dæmi: Stofna reikningsreglur byggt á fjölda tiltekinnar prósentu af loknu verki (handvirkur útreikningur)

Samtakanna í hugbúnað consulting staðfesta, færir inn samningur við viðskiptavin til að þróa hluti afurðar sem viðskiptavinurinn er að þróa. Fyrirtækið samþykkir að afhenda hugbúnaðarkóða yfir sex mánaða tímabil. Viðskiptavinurinn fellst á að greiða fyrirtækið samtals 100.000 fyrir vinnustöðina. Þú stofnar reikningsreglur til að reikningsfæra viðskiptavin byggt á þeirri prósentu vinnu sem er lokið á verkið eins og tilgreint er í samningnum.

-   Í lok fyrsta mánaðar, þú hittir viðskiptavininn til að ákvarða hversu stóru hlutfalli vinnu sé lokið. Eftir að þú og viðskiptavinur hafið gert skoðun á verkinu ákveður þú að verkinu sé 15 prósent lokið.
-   Þú stofnar reikning fyrir 15,000 (15 prósent af 100.000) og sendir hann til viðskiptavinarins.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Dæmi: Stofna reikningsreglur byggðar á fjölda tiltekinnar prósentu af loknu verki (sjálfvirkur útreikningur)

Fyrirtæki þitt, sem er í hugbúnaðarþróun, samþykkir að þróa launabókhaldspakka fyrir viðskiptavinar fyrir 30.000. Viðskiptavinurinn fellst á að greiða fyrirtækið byggðar á prósentu vinnu sem lokið. Verkkostnaður er 20,000 er metin. Verksamningurinn tilgreinir þær tegundir vinnu sem þú getur notað í reikningagerð. Setja upp er reglur sem reikningsfæra sjálfkrafa reikningsupphæðir fyrir hlutfall vinnu sem er lokið fyrir hverja tegund. Hægt er að setja upp fjárhagsáætlunar fyrir hverja tegund:

-   **Þróun** – Kostnaður 15.000 og tekjur af 20.000
-   **Uppsetning** - Kostnaður 5.000 og tekjur upp á 10.000

Þegar reikningur viðskiptavinar er stofnaður í fyrsta sinn er reikningsupphæð sjálfkrafa reiknuð út frá eftirfarandi upplýsingum:

-   Eftir mánuð, starfsmanns í verki sendir vinnukort fyrir verk. Kostnaður við tíma starfsmanns er 5.000 fyrir þróun og 1.000 fyrir uppsetningu. Þróunarvinnu er 33 prósenta (5.000 raunveruleg kostnaðar/15.000 kostnað fjárhagsáætlunar) og uppsetningarvinnu er 20 prósent lokið (1.000 raunveruleg kostnaðar/5.000 kostnað fjárhagsáætlunar).
-   Reikningsupphæð 8,667 er sjálfkrafa reiknaður (hlutfall (33 prósent 20,000 plús 20% af 10.000).
-   Þú stofnar reikning fyrir 8,667 og sendir hann til viðskiptavinarins.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Dæmi: Stofna reikningsreglur sem eru byggðar á þáttaskilum samkvæmt samkomulagi

Fyrirtækið, ráðgjöf fyrir birgðastjórnun, samþykkir að framkvæma markaðsrannsókn á neytendaafurð sem viðskiptamaður hyggst selja. Viðskiptavinurinn fellst á að nota við þjónustu fyrir þriggja mánaða tímabil hefst í Mars og samþykkir að borga fyrirtækið 50.000. Verkið eru þrír áfangar:

-   1. áfangi: Safna neytendagögnum – 31. mars
-   2. áfangi: Greina neytendagögn – 30. apríl
-   3. áfangi: Leggja fram tillögu um lífvænleika afurðar – 31. maí

Viðskiptavinurinn fellst á að greiða fyrirtæki þínu 10.000 fyrir fyrsta þáttaskil og 20,000 fyrir annað þáttaskil, og 20.000 fyrir þriðju þáttaskil. 

Þegar settur er upp verksamningur samþykkir þú að rukka viðskiptavininn byggt loknum áfanga. Reikningsregluuppsetningin inniheldur eftirfarandi skref:

-   Skilgreina áfanga verks.
-   Skilgreina upphæðina sem á að reikningsfæra á viðskiptavininn þegar hverju þáttaskil er lokið.

Þegar fyrsta þáttaskil lýkur 31. Mars, merkirðu þáttaskilunum sé lokið og stofna síðan reikning fyrir 10.000 og senda hann til viðskiptavinar. Ekki er hægt að stofna reikning fyrir þáttaskil þar til búið er að merkja þáttaskilunum sé lokið.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Dæmi: Stofna reikningsreglur sem eru byggðar á þjónustu plús stjórnunargjald

Fyrirtækið þitt, ráðgjafafyrirtæki í stjórnun, fellst á að framkvæma rannsóknir á markaði til að meta sýnileika afurðar sem viðskiptavinur, smásölufyrirtæki, er að þróa. Samningsatriði tilgreina að þú munir veita þjónustu þriggja háttsettra stjórnunarráðgjafa til þess að framkvæma rannsóknina á tíma- og efni. Viðskiptamaðurinn fellst á að borga 100 á klukkustund auk 10 prósent viðbótar stjórnunarþóknun fyrir tíma ráðgjafans sem eru skuldfærðir á verkið. 

Þegar settur er upp verksamningur, skal stofna reikningsreglur til að bæta 10 prósenta stjórnunargjaldi við ráðgjafartíma sem er gjaldfærð á verk. 

Þegar þú stofnar reikning fyrir viðskiptavin, er viðskiptavinurinn krafinn um 10 prósent stjórnunarþóknun auk tímakostnaðar við ráðgjöf. Til dæmis, ef þrír utanaðkomandi ráðgjöfum unnu samtals 200 klukkustundir í verki, reikningur er búinn til uppá 22.000, á eftirfarandi útreikningum.

-   200 klukkustundir með 100 á klukkustund = 20.000
-   10 prósent stjórnunarþóknun = 2000
-   Heildarupphæð reiknings = 22.000

Ef þóknanir eru skattskyldar til viðskiptavinar og þú velur vsk-flokk í verksamningnum,er vsk-flokki sjálfkrafa færður inn í á reikningsreglu fyrir þóknun.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Til dæmis: Stofna reikningsreglur gildi tíma og efnis

Fyrirtæki þitt, hugbúnaðarráðgjafafyrirtæki, samþykkir að veita fimm tæknilega ráðgjafa til að vinna að hugbúnaðarþróunarverkefni fyrir viðskiptavin í næstu sex mánuði. Viðskiptavinurinn fellst á að greiða 150 fyrir hverja ráðgjafatíma sem og kostnað fyrir skrifstofuvörur. Fyrirtækið sendir reikning til viðskiptavinar í lok hvers mánaðar. 

Þegar settur er upp verksamningur, samþykkir þú að rukka viðskiptavininn mánaðarlega fyrir tíma og efni á verki. Að stofna reikningsreglur sem inniheldur eftirfarandi upplýsingar:

-   Samningstímabil er sex mánuðir.
-   Ráðgjafartíma er reiknaður á virðinu 150 á klukkustund.
-   Skrifstofuvörur eru reikningsfærð á kostnaðarverði, og heildarkostnaður fyrir verkið má ekki fara yfir 10.000.
-   Stofna reikning viðskiptavinar í lok hvers almanaksmánaðar á meðan verki stendur.

Fyrsta mánuð samtals 800 klukkustundir eru skráð hjá utanaðkomandi ráðgjöfum í verkinu. Kostnaður skrifstofuvörur sem gjaldfærðir eru á verkið er 2.000. Þessvegna, Í lok mánaðarins stofnar þú reikning upp á 122.000, reiknað sem 800 klukkustundir með 150 á klst. plús 2.000 fyrir skrifstofuvörur.




