---
title: Vegið meðaltal með efnislegt virði og merkingu
description: Vegið meðaltal er birgðalíkan sem byggist á reglunni um vegið meðaltal, þar sem úthreyfingar úr birgðum eru metnar á meðalgildi varanna sem tekið er á móti inn í birgðirnar á birgðalokunartímabilinu, auk allra lagerbirgða úr fyrra tímabili.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c80dcdc08432bb68478827c8763735e644aa4a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675264"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Vegið meðaltal með efnislegt virði og merkingu

[!include [banner](../includes/banner.md)]

Vegið meðaltal er birgðalíkan byggt á meðaltali sem verður til út frá margföldun á hverjum þætti (vörufærslu) með stuðli (kostnaðarverði) sem endurspeglar mikilvægi þess (magn). Önnur leið til að segja þetta er að vegið meðaltal er birgðalíkan sem úthlutar kostnaði við útgáfufærslur sem byggist á meðalvirði allra birgða sem borist hafa á tímabilinu, auk lagerbirgða frá fyrra tímabili.

Þegar birgðalokun er keyrð með birgðalíkani vegins meðaltals er hægt að búa til jöfnun á tvennan hátt. Yfirleitt eru allar innhreyfingar jafnaðar á móti sýndarúthreyfingu sem geymir heildarmagn og virði móttekins magns. Þessi sýndarúthreyfing hefur samsvarandi sýndarinnhreyfingu þaðan sem úthreyfingar eru jafnaðar. Þannig fá allar úthreyfingar sama meðalkostnað. Sýndarúthreyfinguna og -innhreyfinguna er hægt að sjá sem sýndarfærslu sem kallast flutningur fyrir *vegið meðaltal birgðalokunar*. Þessi jöfnunaraðferð er þekkt sem *samantekin jöfnun vegins meðaltals*. Ef aðeins er um að ræða innhreyfingu er hægt að jafna allar úthreyfingar þaðan og sýndarfærslan verður ekki útbúin. Þessi jöfnunaraðferð er kölluð *bein jöfnun*. Allar birgðir sem eru á lager eftir birgðalokun eru metnar sem vegið meðaltal frá fyrra tímabili og teknar með í útreikningi vegins meðaltals á næsta tímabili.

Hægt er að hnekkja reglunni um vegið meðaltal með því að merkja birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu. Reglubundin birgðalokun er nauðsynleg þegar notað er birgðalíkan vegins meðaltals til að búa til uppgjör og breyta gildi úthreyfinga í samræmi við reglu vegins meðaltals. Þar til þú keyrir birgðalokunarferli, eru úthreyfingarfærslur metnar á hlaupandi meðaltali þegar efnislegar og fjárhagslegar uppfærslur áttu sér stað. Nema ef merking er notuð þá er hlaupandi meðaltal reiknað út þegar efnisleg eða fjárhagsleg uppfærsla er framkvæmd.

Aðferð birgðalokunar með vegnu meðaltali er reiknuð út með eftirfarandi formúlu:

- Vegið meðaltal = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = Magn færslu  
P = Verð færslunnar

Jafnanir eru birgðalokunarbókanir sem leiðrétta úthreyfingar í rétt vegin meðaltöl frá og með lokadagsetningunni. Eftirfarandi dæmi skýra áhrif þess að nota vegið meðaltal með fimm ólíkum skilgreiningum:

- Bein jöfnun vegins meðaltals án valkostinum **Taka efnislegt virði** með
- Samantektarjöfnun vegins meðaltals án valkostarins **Taka efnislegt virði** með
- Bein jöfnun vegins meðaltals með valkostinum **Taka efnislegt virði** með
- Samantektarjöfnun vegins meðaltals með valkostinum **Taka efnislegt virði** með
- Vegið meðaltal með merkingu

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Bein jöfnun vegins meðaltals án þess að taka efnislegt virði með

Reglan um beina jöfnun býr til jafnanir beint á milli innhreyfing og úthreyfinga, án þess að búa til viðbótarbirgðafærslur. Kerfið notar þessa reglu beinnar jöfnunar í eftirfarandi aðstæðum:

- Ein innhreyfing og eitt eða fleiri vandamál hafa verið bókaðar á þessu tímabili.
- Einungis úthreyfingar hafa verið bókaðar á tímabilinu og birgðir innihalda vörur á lager frá fyrri lokun

Í þessu dæmi er gátreiturinn **Taka efnislegt virði með** hreinsaður á **Vörulíkanaflokkur** fyrir vöruna sem er losuð. Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 10 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 20,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 10,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 10,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 4a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 4b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 5a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 6\. Birgðalokun er framkvæmd. Samkvæmt aðferð vegins meðaltals notar kerfið beina jöfnunaraðferð vegna þess að aðeins ein innhreyfing er uppfærð fjárhagslega á tímabilinu. Í þessu dæmi er ein jöfnun búin til á milli 1b og 3b og önnur á milli 1b og 4b. Engin leiðrétting er gerð vegna þess að hlaupandi meðaltal er það sama og vegið meðaltal.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun án valkostarins **Taka með efnislegt virði**.

![WeightedAverage beinnar jöfnunar án Taka efnislegt virði með.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Samantektarjöfnun vegins meðaltals án valkostarins Taka efnislegt virði með

Þegar margar innhreyfingar eru á tilteknu tímabili notar vegið meðaltal reglu samantekinnar jöfnunar þar sem allar innhreyfingar á lokunartímabili eru teknar saman í færslu sem er nefnd *vegið meðaltal birgðalokunar*. Öll innhreyfing dagsins verður gerð upp gegn úthreyfingu nýrra birgðafærslna. Öll úthreyfing dagsins verður gerð upp gegn innhreyfingu nýrra birgðafærslna. Ef birgðavirði er eftir á lager eftir birgðalokun er birgðavirði á lager innifalið í innhreyfingarfærslu í vegnu meðaltali birgðalokunarfærslna.

Eftirfarandi færslur birtast á myndinni hér fyrir neðan:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 16,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 23,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 7\. Birgðalokun er framkvæmd.
- 7a. Fjárhagslega úthreyfingin Birgðalokunarfærsla vegins meðaltals er stofnuð til að leggja saman jafnanir allra fjárhagslegu innhreyfinga birgðanna.
  - Færsla 1b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 10,00 USD.
  - Færsla 2b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 22,00 USD.
  - Færsla 5b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 30,00 USD.
  - Færsla 7a. er búin til fyrir magn 3 með jafnaða upphæð 62,00 USD. Þessi færsla vegur upp á móti summu þriggja útgáfufærsla sem er uppfærð fjárhagslega á tímabilinu.
- 7b. Fjárhagslega innhreyfingin Birgðalokunarfærsla vegins meðaltals er stofnuð sem mótvægi við fjárhagslega bókaðar innhreyfingar.
  - Færsla 3b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 20,67 USD. Þessi færsla er leiðrétt um 4,67 USD til að færa upphaflegt gildi 16,00 USD í 20,67 USD sem er vegið meðaltal á fjárhagslega bókuðum færslum fyrir tímabilið.
  - Færsla 7b. er búin til fyrir magn 1 með jafnaða upphæð 20,67 USD til að vega upp á móti 3b. Þessi færsla vegur upp á móti summu einnar útgáfufærslu sem er uppfærð fjárhagslega á tímabilinu.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun án valkostarins **Taka með efnislegt virði**.

![Vegið meðaltal samantekinnar jöfnunar án Taka efnislegt virði með.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Bein jöfnun vegins meðaltals með valkostinum Taka efnislegt virði með

Færibreytan **Taka með efnislegt virði** virkar öðruvísi með birgðalíkani vegins meðaltals en í öðrum útgáfum vörunnar. Þegar valkosturinn **Efnislegt virði tekið með** er valinn fyrir vöru í skjámyndinni **Vörulíkanaflokkur** notar kerfið efnislega uppfærðar innhreyfingar þegar það reiknar út áætlað kostnaðarverð úthreyfingar eða hlaupandi meðaltal. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Í birgðalokuninni verða aðeins fjárhagslega uppfærðar innhreyfingar hafðar í huga í útreikningi vegins meðaltals.

Eftirfarandi færslur birtast á myndinni hér fyrir neðan:

- 1a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 10 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 20,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 15,00 USD (hlaupandi meðaltal fjárhagslega og efnislegra bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 15,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 4a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 15,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 4b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 15,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 5a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 15,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 6\. Birgðalokun er framkvæmd. Samkvæmt aðferð vegins meðaltals notar kerfið beina jöfnunaraðferð vegna þess að aðeins ein innhreyfing er uppfærð fjárhagslega á tímabilinu. Í þessu dæmi er ein jöfnun búin til á milli 1b og 3b og önnur á milli 1b og 4b. Færslur 3b og 4b eru leiðréttar um -5,00 USD til að færa virðið í 10,00 USD.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun með valkosti **Taka með efnislegt virði**.

![Vegið meðaltal beinnar jöfnunar með Taka efnislegt virði með.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Samantektarjöfnun vegins meðaltals með valkostinum Taka efnislegt virði með

Færibreytan **Taka með efnislegt virði** virkar öðruvísi með birgðalíkani dagsetningar vegins meðaltals  en í öðrum útgáfum. Veldu gátreitinn **Taka efnislegt virði með** fyrir vöru á síðunni **Vörulíkanaflokkur**. Kerfið mun svo efnislega uppfærðar innhreyfingar þegar áætlað kostnaðarverð eða meðaltal er reiknað út. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Í birgðalokuninni verða aðeins fjárhagslega uppfærðar innhreyfingar hafðar í huga í útreikningi vegins meðaltals. Við mælum með mánaðarlegri birgðalokun þegar notað er birgðalíkanið með vegið meðaltal. Í þessu dæmi um samantektarjöfnun á vegnu meðaltali, er birgðalíkanið merkt til að innihalda efnislega virðið.

Eftirfarandi færslur birtast á myndinni hér fyrir neðan:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD (hlaupandi meðaltal fjárhagslega og efnislegra bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 23,67 USD (hlaupandi meðaltal fjárhagslega og efnislegra bókaðra færslna).
- 7\. Birgðalokun er framkvæmd.
- 7a. Fjárhagslega úthreyfingin Birgðalokunarfærsla vegins meðaltals er stofnuð til að leggja saman jafnanir allra fjárhagslegu innhreyfinga birgðanna.
  - Færsla 1b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 10,00 USD.
  - Færsla 2b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 22,00 USD.
  - Færsla 5b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 30,00 USD.
  - Færsla 7a. er búin til fyrir magn 3 með jafnaða upphæð 62,00 USD.  
- 7b. Fjárhagslega innhreyfingin „Birgðalokunarfærsla vegins meðaltals“ er stofnuð sem mótvægi við fjáhagslega lokaðar úthreyfingarfærslur.
  - Færsla 3b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 20,67 USD. Þessi færsla er leiðrétt um 4,67 USD til að færa upphaflegt gildi 16,00 USD í 20,67 USD sem er vegið meðaltal á fjárhagslega bókuðum færslum fyrir tímabilið.
  - Færsla 7b. er búin til fyrir magn 1 með jafnaða upphæð 20,67 USD til að vega upp á móti 3b.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun án valkostarins **Taka með efnislegt virði**.

![WeightedAverage samantekinnar jöfnunar með Taka efnislegt virði með.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-with-marking"></a>Vegið meðaltal með merkingu

Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar ætlunin er að ganga úr skugga um nákvæman kostnað við birgðir þegar færsla er bókuð eða þegar birgðalokun er framkvæmd.

Þjónustudeild fyrir viðskiptavini, hefur til dæmis fengið flýtipöntun frá mikilvægum viðskiptavini. Þar sem um flýtipöntun er að ræða þarf að greiða meira fyrir vöruna til þess að geta mætt beiðni viðskiptavinarins. Þú verður að vera viss um að kostnaður þessa birgðavara endurspeglast í framlegðinni, eða kostnaður seldra vara (COGS), fyrir þessa sölupöntunarreikning.

Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Til dæmis, þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður. Síðan er kostnaður seldra VARA 120,00 USD í staðinn fyrir núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði.

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra.

Innhreyfingarfærsla er merkt við úthreyfingarfærslu. Þá er matsaðferðin sem valin er fyrir birgðalíkanaflokk vörunnar hunsaður og kerfið mun jafna þessar færslur hvor við aðra.

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þetta frá sölupöntunarlínu á síðunni **Ítarupplýsingar sölupöntunar**. Opnar innhreyfingarfærslur eru skoðaðar á síðunni **Merking**.

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók.

Eftirfarandi færslur birtast á myndinni hér fyrir neðan:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 16,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3c. Fjárhagsleg úthreyfing birgða fyrir 3b er merkt við fjárhagslega úthreyfing birgða fyrir 2b.
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 23,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 7\. Birgðalokun er framkvæmd. Samkvæmt merkingarreglunni sem notar aðferðina vegið meðaltal eru merktu færslurnar jafnaðar á móti hvor annarri. Í þessu dæmi er 3b gerð upp á móti 2b og leiðrétting fyrir 6,00 USD er sett inn á 3b til að færa gildið í 22,00 USD. Í þessu dæmi eru engin viðbótarjafnanir gerð vegna þess að lokunin skapar einungis jafnanir fyrir fjárhagslega uppfærðar færslur.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum og áhrifum þess að merkja við birgðalíkan vegins meðaltals.

![Vegið meðaltal með Merkingu.](media/weighted-average-with-marking.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
