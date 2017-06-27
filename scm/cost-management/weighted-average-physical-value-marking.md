---
title: "Vegið meðaltal með efnislegu virði og marki"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cdbca6d9c71c901a1f4e7a8e5a2f9be1d3efb355
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="weighted-average-with-physical-value-and-marking"></a>Vegið meðaltal með efnislegu virði og marki

[!include[banner](../includes/banner.md)]




Þegar birgðalokun er keyrð eru allar móttökur jafnaðar gagnvart sýndarúthreyfingum sem geyma heildar mótekið magn og virði. Þessi sýndarúthreyfing hefur samsvarandi sýndarinnhreyfingu þaðan sem úthreyfingar eru jafnaðar. Þannig fá allar úthreyfingar sama meðalkostnað. Sýndarúthreyfinguna og -innhreyfinguna er hægt að sjá sem sýndarfærslu sem kallast flutningur fyrir vegið meðaltal birgðalokunar

Ef aðeins er um að ræða innhreyfingu er hægt að jafna allar úthreyfingar þaðan og sýndarfærslan verður ekki útbúin. 

Þegar vegið meðaltal er notað geturðu merkt birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu í stað þess að nota regluna um vegið meðaltal. 

Við mælum með mánaðarlegri birgðalokun þegar þú notar birgðalíkanið vegið meðaltal. 

Aðferð birgðalokunar með vegnu meðaltali er reiknuð út með eftirfarandi formúlu:
-   Vegið meðaltal = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Birgðafærslur sem fara frá birgðaúthreyfingum. Þetta felur í sér að sölupantanir, birgðabækur, og framleiðslupantanir, eiga sér stað á áætluðu kostnaðarverði á dagsetningu bókunar. Þetta áætlaða kostnaðarverð er einnig kallað meðalverð. Við birgðalokun mun kerfið greina birgðafærslur fyrir fyrri og gildandi tímabil og ákvarða hvaða eftirfarandi lokunaraðferð eigi að nota.
-   Bein jöfnun
-   Samantektarjöfnun

Jafnanir eru birgðalokunarbókanir sem leiðrétta úthreyfingar í rétt vegin meðaltöl frá og með lokadagsetningunni. Eftirfarandi dæmi skýra áhrif þess að nota vegið meðaltal með fimm ólíkum skilgreiningum:
-   Bein jöfnun vegins meðaltals án valkostinum Taka efnislegt virði með
-   Samantektarjöfnun vegins meðaltals án valkostarins Taka efnislegt virði með
-   Bein jöfnun vegins meðaltals með valkostinum Taka efnislegt virði með
-   Samantektarjöfnun vegins meðaltals með valkostinum Taka efnislegt virði með
-   Vegið meðaltal með merkingu

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Bein jöfnun vegins meðaltals án þess að taka efnislegt virði með
Reglan um beina jöfnun er sú sama og notuð er fyrir vegið meðaltal í fyrri útgáfum. Kerfið mun jafna beint á milli innhreyfinga og úthreyfinga. Kerfið notar þessa reglu beinnar jöfnunar í ákveðnum aðstæðum:
-   Ein innhreyfing og ein eða margar úthreyfingar hafa verið bókaðar á þessu tímabili
-   Einungis úthreyfingar hafa verið bókaðar á tímabilinu og birgðir innihalda vörur á lager frá fyrri lokun

Í aðstæðunum fyrir neðan hafa fjárhagslega uppfærðar innhreyfingar og úthreyfingar verið bókaðar. Á meðan á birgðalokun stendur mun kerfið gera upp innhreyfingu beint á móti úthreyfingu og ekki er nauðsynlegt að leiðrétta kostnaðarverð við úthreyfingu. Eftirfarandi færslur birtast á myndinni hér fyrir neðan:
-   1a. Efnisleg innhreyfing uppfærð fyrir magnið 5 á 10,00 USD hver
-   1b. Fjárhagsleg innhreyfing uppfærð fyrir magnið 5 á 10,00 USD hver
-   2a. Efnisleg úthreyfing uppfærð fyrir magnið 2 á 10,00 USD hver
-   2b. Fjárhagsleg úthreyfing uppfærð fyrir magnið 2 á 10,00 USD hver
-   3. Birgðalokun er framkvæmd með því að nota beina jöfnunaraðferð til að jafna fjárhagslega innhreyfingu birgða í fjárhagslega úthreyfingu birgða.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun án valkostarins taka með efnislegt virði. 

![Vegið meðaltal beinnar jöfnunar án Taka efnislegt virði með](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Lykill að skýringarmynd**
-   Birgðafærslur eru táknaðar með lóðréttum örvum.
-   Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
-   Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
-   Fyrir ofan (eða fyrir neðan) hverja lóðrétta ör er virði birgðafærslu tilgreint í sniðinu Quantity@Unitprice.
-   Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
-   Virði birgðafærslu án hornklofa táknar að birgðafærslan er bókuð fjárhagslega í birgðir.
-   Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
-   Hver lóðrétt ör er merkt með raðkenni, til dæmis *1a*. Kennið gefur bókunarröð birgðafærslna á tímaásnum til kynna.
-   Birgðalokanir eru birtar með rauðri lóðréttri strikalínu og merkinu Birgðalokun.
-   Jafnanir sem eru framkvæmdar af birgðalokun eru birtar með rauðum punktaörum sem fara á ská frá móttöku að úthreyfingu.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Samantektarjöfnun vegins meðaltals án valkostarins Taka efnislegt virði með
Vegið meðaltal notar þá jöfnunarreglu að öll innhreyfing innan lokunartímabils er tekin saman í færslu kallað birgðalokunarfærsla með Vegnu meðaltali. Allar innhreyfingar fyrir tímabilið verða jafnaðar á móti úthreyfingu nýlega stofnaðrar birgðaflutningafærslur. Allar úthreyfingar fyrir tímabilið verða jafnaðar á móti innhreyfingu nýrrar birgðaflutningafærslu. Ef birgðir á lager eru jákvæðar eftir birgðalokunina eru þær birgðir og virði birgðanna tekið saman í nýja birgðaflutningsfærslu (innhreyfing). Ef birgðir á lager eru neikvæðar eftir birgðalokunina eru birgður á lager og virði birgðanna summa einstakra úthreyfinga sem hafa ekki verið jafnaðar að fullu. Í aðstæðunum fyrir neðan hafa nokkrar fjárhagslega uppfærðar innhreyfingar og ein úthreyfing verið bókaðar. 

Í birgðalokun mun kerfið mynda og bóka samanteknu birgðaflutningafærsluna til að jafna allar innhreyfingar fyrir tímabilið á móti samanteknu úthreyfingarfærslu birgðaflutningsins. Allar bókaðar úthreyfingar fyrir tímabilið verða jafnaðar á móti samanteknu innhreyfingarfærslu birgðaflutningsins. Vegið meðaltal reiknast sem 15,00 USD. úthreyfing var upprunalega bókuð með áætluðu kostnaðarverði upp á USD 14.67. Neikvæð leiðrétting upp á 0,33 USD er gerð á og bókuð á úthreyfinguna. Frá og með birgðalokunardegi eru lagerbirgðirnar 3 stykki með virðið 45,00 USD. 

Eftirfarandi færslur eru sýndar í myndrænt fyrir neðan:
-   1a. Efnisleg innhreyfing birgða uppfærð í magnið 2 á kostnaðinum 11,00 USD hver.
-   1b. Fjárhagsleg innhreyfing birgða uppfærð í magnið 2 á kostnaðinum 14,00 USD hver.
-   2a. Efnisleg innhreyfing birgða uppfærð í magnið 1 á kostnaðinum 12,00 USD hver.
-   2b. Fjárhagsleg innhreyfing birgða uppfærða í magnið 1 á kostnaðinum 16,00 USD hver.
-   3a. Efnisleg úthreyfing birgða uppfærð í magnið 1 á kostnaðinum 14,67 USD hver (meðalverð).
-   3b. Fjárhagsleg úthreyfing birgða uppfærð í magnið 1 á kostnaðinum 14,67 USD hver (meðalverð).
-   4a. Efnisleg innhreyfing birgða uppfærð í magnið 1 á kostnaðinum 14,00 USD hver.
-   4b. Fjárhagsleg innhreyfing birgða uppfærða í magnið 1 á kostnaðinum 16,00 USD hver.
-   5. Birgðalokun er framkvæmd.
-   6a. Fjárhagslega úthreyfingin „Birgðalokunarfærsla vegins meðaltals“ er stofnuð til að leggja saman jafnanir allra fjárhagslegu innhreyfinga birgðanna.
-   6b. Fjárhagslega innhreyfingin „Birgðalokunarfærsla vegins meðaltals“ er stofnuð sem mótvægi við 5a.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um samantekna beina jöfnun án valkostarins taka með efnislegt virði. 

![Vegið meðaltal samantekinnar jöfnunar án Taka efnislegt virði með    ](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Lykill að skýringarmynd**
-   Birgðafærslur eru táknaðar með lóðréttum örvum.
-   Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
-   Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
-   Fyrir ofan (eða fyrir neðan) hverja lóðrétta ör er virði birgðafærslu tilgreint í sniðinu Quantity@Unitprice.
-   Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
-   Virði birgðafærslu án hornklofa táknar að birgðafærslan er bókuð fjárhagslega í birgðir.
-   Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
-   Hver lóðrétt ör er merkt með raðkenni, til dæmis *1a*. Kennið gefur bókunarröð birgðafærslna á tímaásnum til kynna.
-   Birgðalokanir eru birtar með rauðri lóðréttri strikalínu og merkinu Birgðalokun.
-   Jafnanir sem eru framkvæmdar af birgðalokun eru birtar með rauðum punktaörum sem fara á ská frá móttöku að úthreyfingu.
-   Rauðar örvar lýsa innhreyfingarfærslum sem verið er að jafna í úthreyfingarfærslu sem stofnuð er af kerfinu.
-   Græna örin táknar mótfærslu kerfismyndaðrar innhreyfingarfærslu þar sem upprunalega bókaða úthreyfingafærslan er jöfnuð

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Bein jöfnun vegins meðaltals með valkostinum Taka efnislegt virði með
Færibreytan Taka með efnislegt virði virkar öðruvísi með birgðalíkani vegins meðaltals en í öðrum útgáfum vörunnar. Veljið gátreit Taka efnislegt virði fyrir vöru í skjámyndinni vörulíkanaflokkur. Kerfið notar efnislega uppfærðar innhreyfingar þegar áætlað kostnaðarverð eða meðaltal er reiknað út. Úthreyfingar eru bókaðar samkvæmt þessu áætlaða kostnaðarverði á tímabilinu. Í birgðalokuninni verða aðeins fjárhagslega uppfærðar innhreyfingar hafðar í huga í útreikningi vegins meðaltals. Við mælum með mánaðarlegri birgðalokun þegar notað er birgðalíkanið með vegið meðaltal. Í þessu dæmi um beina jöfnun á vegnu meðaltali, er birgðalíkanaflokkurinn merktur til að innihalda efnislega virðið. 

Eftirfarandi færslur birtast á myndinni hér fyrir neðan:
-   1a. Efnisleg innhreyfing birgða uppfærð í magnið 1 á kostnaðinum 11,00 USD hver.
-   1b. Fjárhagsleg innhreyfing birgða uppfærð í magnið 1 á kostnaðinum 10,00 USD hver.
-   2a. Efnisleg innhreyfing birgða uppfærð í magnið 1 á kostnaðinum 15,00 USD hver.
-   3a. Efnisleg úthreyfing birgða uppfærð í magnið 1 á kostnaðinum 12,50 USD hver (meðalkostnaður, þar sem reiknað er með efnislegu gildi).
-   3b. Fjárhagsleg úthreyfing birgða uppfærð í magnið 1 á kostnaðinum 12,50 USD hver (meðalkostnaður, fyrst að efnislegt gildi innhreyfingar er haft í huga).
-   4. Birgðalokun er framkvæmd. Í birgðalokuninni mun kerfið hunsa allar birgðafærslur sem hafa aðeins verið efnislega uppfærðar. Í staðinn er notuð bein jöfnunarregla vegna þess að aðeins ein fjárhagsleg innhreyfing er til staðar. Leiðrétting upp á 2,50 USD verður bókuð í birgðafærsluna sem hefur verið fjárhagslega úthreyfð frá og með birgðalokunardagsetningu. Eftir birgðalokun eru lagerbirgðirnar magnið 1 með meðalkostnaðarverðið 15,00 USD.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun með valkosti Hafa með efnislegt virði. 

![Vegið meðaltal beinnar jöfnunar með Taka efnislegt virði með    ](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Lykill að skýringarmynd**
-   Birgðafærslur eru táknaðar með lóðréttum örvum.
-   Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
-   Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
-   Fyrir ofan (eða fyrir neðan) hverja lóðrétta ör er virði birgðafærslu tilgreint í sniðinu Quantity@Unitprice.
-   Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
-   Virði birgðafærslu án hornklofa táknar að birgðafærslan er bókuð fjárhagslega í birgðir.
-   Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
-   Hver lóðrétt ör er merkt með raðkenni, til dæmis *1a*. Kennið gefur bókunarröð birgðafærslna á tímaásnum til kynna.
-   Birgðalokanir eru birtar með rauðri lóðréttri strikalínu og merkinu Birgðalokun.
-   Jafnanir sem eru framkvæmdar af birgðalokun eru birtar með rauðum punktaörum sem fara á ská frá móttöku að úthreyfingu.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Samantektarjöfnun vegins meðaltals með valkostinum Taka efnislegt virði með
Færibreytan Taka með efnislegt virði virkar öðruvísi með birgðalíkani dagsetningar vegins meðaltals  en í öðrum útgáfum. Veljið gátreit Taka efnislegt virði fyrir vöru með í skjámyndinni vörulíkanaflokkur. Kerfið mun svo efnislega uppfærðar innhreyfingar þegar áætlað kostnaðarverð eða meðaltal er reiknað út. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Í birgðalokuninni verða aðeins fjárhagslega uppfærðar innhreyfingar hafðar í huga í útreikningi vegins meðaltals. Við mælum með mánaðarlegri birgðalokun þegar notað er birgðalíkanið með vegið meðaltal. Í þessu dæmi um samantektarjöfnun á vegnu meðaltali, er birgðalíkanið merkt til að innihalda efnislega virðið. 

Eftirfarandi færslur eru sýndar í myndrænt fyrir neðan:
-   1a. Efnisleg innhreyfing birgða uppfærð í magnið 2 á kostnaðinum 11,00 USD hver.
-   1b. Fjárhagsleg innhreyfing birgða uppfærð í magnið 2 á kostnaðinum 14,00 USD hver.
-   2. Efnisleg innhreyfing birgða uppfærð í magnið 1 á kostnaðinum 10,00 USD hver.
-   3a. Efnisleg innhreyfing birgða uppfærð í magnið 1 á kostnaðinum 12,00 USD hver.
-   3b. Fjárhagsleg innhreyfing birgða uppfærða í magnið 1 á kostnaðinum 16,00 USD hver.
-   4a. Efnisleg úthreyfing birgða uppfærð í magnið 1 á kostnaðinum 13,50 USD hver (meðalkostnaður, þar sem reiknað er með efnislegu gildi).
-   4b. Fjárhagsleg úthreyfing birgða uppfærð í magnið 1 á kostnaðinum USD 13,50 hver (meðalkostnaður, fyrst að efnislegt gildi innhreyfingar er haft í huga).
-   5a. Efnisleg innhreyfing birgða uppfærð í magnið 1 á kostnaðinum 14,00 USD hver.
-   5b. Fjárhagsleg innhreyfing birgða uppfærða í magnið 1 á kostnaðinum 16,00 USD hver.
-   6. Birgðalokun er framkvæmd. Í birgðalokuninni mun kerfið hunsa allar birgðafærslur sem hafa aðeins verið uppfærðar efnislega. Samantektarjöfnunarregla er notuð vegna þess að aðeins ein fjárhagsleg innhreyfing er til staðar. Leiðrétting upp á 1,50 USD verður bókuð í birgðafærsluna sem hefur verið fjárhagslega úthreyfð frá og með birgðalokunardagsetningu. Eftir birgðalokun eru lagerbirgðirnar magnið 3 með meðalkostnaðarverðið 15,00 USD.
-   7a. Fjárhagslega úthreyfingin „Birgðalokunarfærsla vegins meðaltals“ er stofnuð til að leggja saman jafnanir allra fjárhagslegu innhreyfinga birgðanna.
-   7b. Fjárhagslega innhreyfingin „Birgðalokunarfærsla vegins meðaltals“ er stofnuð sem mótvægi við 5a.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun án valkostarins taka með efnislegt virði. 

![Vegið meðaltal samantekinnar jöfnunar með Taka efnislegt virði með    ](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Lykill að skýringarmynd**
-   Birgðafærslur eru táknaðar með lóðréttum örvum.
-   Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
-   Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
-   Fyrir ofan (eða fyrir neðan) hverja lóðrétta ör er virði birgðafærslu tilgreint í sniðinu Quantity@Unitprice.
-   Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
-   Virði birgðafærslu án hornklofa táknar að birgðafærslan er bókuð fjárhagslega í birgðir.
-   Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
-   Hver lóðrétt ör er merkt með raðkenni, til dæmis 1a. Kennið gefur bókunarröð birgðafærslna á tímaásnum til kynna.
-   Birgðalokanir eru birtar með rauðri lóðréttri strikalínu og merkinu Birgðalokun.
-   Jafnanir sem eru framkvæmdar af birgðalokun eru birtar með rauðum punktaörum sem fara á ská frá móttöku að úthreyfingu.
-   Rauðar örvar lýsa innhreyfingarfærslum sem verið er að jafna í úthreyfingarfærslu sem stofnuð er af kerfinu.
-   Græna örin táknar mótfærslu kerfismyndaðrar innhreyfingarfærslu þar sem upprunalega bókaða úthreyfingafærslan er jöfnuð

## <a name="weighted-average-with-marking"></a>Vegið meðaltal með merkingu
Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar ætlunin er að ganga úr skugga um nákvæman kostnað við birgðir þegar færsla er bókuð eða þegar birgðalokun er framkvæmd. 

Þjónustudeild fyrir viðskiptavini, hefur til dæmis fengið flýtipöntun frá mikilvægum viðskiptavini. Þar sem um flýtipöntun er að ræða þarf að greiða meira fyrir vöruna til þess að geta mætt beiðni viðskiptavinarins. Þú verður að vera viss um að kostnaður þessa birgðavara endurspeglast í framlegðinni, eða kostnaður seldra vara (COGS), fyrir þessa sölupöntunarreikning. 

Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Til dæmis, þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður. Síðan er kostnaður seldra VARA 120,00 USD í staðinn fyrir núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði. 

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra. 

Innhreyfingarfærsla er merkt við úthreyfingarfærslu. Þá er matsaðferðin sem valin er fyrir birgðalíkanaflokk vörunnar hunsaður og kerfið mun jafna þessar færslur hvor við aðra. 

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þetta frá sölupöntunarlínu á síðunni Ítarupplýsingar sölupöntunar. Opnar innhreyfingarfærslur eru skoðaðar á síðunni Merking. 

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók. 

Eftirfarandi færslur birtast á myndinni hér fyrir neðan:
-   1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
-   1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
-   2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
-   2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 20,00 USD á hverja.
-   3a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
-   4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
-   4b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
-   5a. Efnisleg úthreyfing birgða í magninu 1 á kostnaðarverði 21,25 USD (meðalverð fjárhagslega og efnislegra uppfærðra færslna).
-   5b. Fjárhagsleg úthreyfing birgða í magninu 1 er merkt við birgðainnhreyfingu 2b áður en færslan er bókuð. Þessi færsla er bókuð með kostnaðarverðinu 20,00 USD.
-   6a. Efnisleg úthreyfing birgða í magninu 1 á kostnaðarverðinu 21,25 USD hver.
-   7 Birgðalokun er framkvæmd. Fyrst að fjárhagslega uppfærða færslan er merkt við innhreyfingu sem fyrir er, eru þessar færslur jafnaðar hvor við aðra og engin leiðrétting er gerð.

Nýtt meðaltal kostnaðarverðs endurspeglar meðaltal færslna sem hafa verið uppfærðar fjárhagslega og efnislega á 27,50 USD. 

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum og áhrifum þess að merkja við birgðalíkan vegins meðaltals. 

![Vegið meðaltal með Merking](./media/weightedaveragewithmarking.gif) 

**Lykill að skýringarmynd**
-   Birgðafærslur eru táknaðar með lóðréttum örvum.
-   Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
-   Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
-   Fyrir ofan (eða fyrir neðan) hverja lóðrétta ör er virði birgðafærslu tilgreint í sniðinu Quantity@Unitprice.
-   Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
-   Virði birgðafærslu án hornklofa táknar að birgðafærslan er bókuð fjárhagslega í birgðir.
-   Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
-   Hver lóðrétt ör er merkt með raðkenni, til dæmis *1a*. Kennið gefur bókunarröð birgðafærslna á tímaásnum til kynna.
-   Birgðalokanir eru birtar með rauðri lóðréttri strikalínu og merkinu Birgðalokun.
-   Jöfnun sem er gerð af birgðalokun er táknuð með brotinni línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.






