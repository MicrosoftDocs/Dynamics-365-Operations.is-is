---
title: Vegið meðaltal með efnislegt virði og merkingu
description: Vegið meðaltal er birgðalíkan sem byggist á reglunni um vegið meðaltal, þar sem úthreyfingar úr birgðum eru metnar á meðalgildi varanna sem tekið er á móti inn í birgðirnar á birgðalokunartímabilinu, auk allra lagerbirgða úr fyrra tímabili.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c124716b70be837573506a738ef2034397f2bda
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330227"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Vegið meðaltal með efnislegt virði og merkingu

[!include [banner](../includes/banner.md)]

Vegið meðaltal er birgðalíkan sem byggir á meðaltali sem leiðir af margföldun hvers þáttar (vöruviðskipti) með stuðli (kostnaðarverð) sem endurspeglar mikilvægi hans (magn). Önnur leið til að segja þetta er að vegið meðaltal er birgðalíkan sem úthlutar kostnaði við útgáfufærslur út frá meðalgildi allra birgða sem mótteknar hafa verið á tímabilinu, að viðbættum birgðum á lager frá fyrra tímabili.

Þegar þú keyrir birgðalokun með því að nota vegið meðaltal birgðalíkansins, eru tvær leiðir til að stofna uppgjör. Venjulega eru allar kvittanir jafnaðar á móti sýndarútgáfu, sem geymir heildarmagn og verðmæti móttekins. Þessi sýndarúthreyfing hefur samsvarandi sýndarinnhreyfingu þaðan sem úthreyfingar eru jafnaðar. Þannig fá allar úthreyfingar sama meðalkostnað. Líta má á sýndarútgáfuna og kvittunina sem sýndarflutning, sem heitir *vegið meðaltal birgðalokunarflutnings*. Þessi uppgjörsaðferð er kölluð a *vegið meðaltal yfirlits uppgjörs*. Ef aðeins er um að ræða innhreyfingu er hægt að jafna allar úthreyfingar þaðan og sýndarfærslan verður ekki útbúin. Þessi uppgjörsaðferð er nefnd a *beint uppgjör*. Allar birgðir sem eru til staðar eftir að birgðalokun er framkvæmd eru metnar á vegið meðaltal frá fyrra tímabili og innifalið í útreikningi vegins meðaltals á næsta tímabili.

Hægt er að hnekkja meginreglunni um vegið meðaltal með því að merkja birgðafærslur þannig að tiltekin vörumóttaka sé jöfnuð á móti tiltekinni útgáfu. Reglubundin birgðalokun er nauðsynleg þegar vegið meðaltal birgðalíkansins er notað til að stofna uppgjör og leiðrétta verðmæti útgáfur í samræmi við meginregluna um vegið meðaltal. Þar til þú keyrir birgðalokunarferlið eru útgáfufærslur metnar á hlaupandi meðaltali þegar líkamlegar og fjárhagslegar uppfærslur áttu sér stað. Nema þú sért að nota merkingu er hlaupandi meðaltal reiknað út þegar líkamleg eða fjárhagsleg uppfærsla er framkvæmd.

Aðferð birgðalokunar með vegnu meðaltali er reiknuð út með eftirfarandi formúlu:

- Vegið meðaltal = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = magn viðskipta  
P = verð viðskipta

Jafnanir eru birgðalokunarbókanir sem leiðrétta úthreyfingar í rétt vegin meðaltöl frá og með lokadagsetningunni. Eftirfarandi dæmi skýra áhrif þess að nota vegið meðaltal með fimm ólíkum skilgreiningum:

- Vegið meðaltal beint uppgjörs án þess **Taktu með líkamlegt gildi** valmöguleika
- Vegið meðaltal samantektar uppgjörs án þess **Taktu með líkamlegt gildi** valmöguleika
- Vegið meðaltal beint uppgjör við **Taktu með líkamlegt gildi** valmöguleika
- Vegið meðaltal samantekið uppgjör við **Taktu með líkamlegt gildi** valmöguleika
- Vegið meðaltal með merkingu

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Bein jöfnun vegins meðaltals án þess að taka efnislegt virði með

Reglan um bein uppgjör stofnar uppgjör beint á milli innhreyfinga og útgáfu án þess að stofna viðbótarbirgðafærslur. Kerfið notar þessa beinu uppgjörsreglu við eftirfarandi aðstæður:

- Ein kvittun og eitt eða fleiri tölublöð hafa verið bókuð á tímabilinu.
- Einungis hefur verið bókað útgáfur á tímabilinu og í birgðum eru tilbúnir hlutir frá fyrri lokun.

Í þessu dæmi er **Taktu með líkamlegt gildi** gátreiturinn er hreinsaður á **Vörulíkanahópur** fyrir útgefna vöruna. Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 10 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 20,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 10.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 10.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 4a. Raunveruleg útgáfa birgða fyrir magn af 1 á kostnaði USD 10.00 hver (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 4b. Fjárhagsútgáfa birgða fyrir magn 1 á kostnaði USD 10.00 hver (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 5a. Raunveruleg útgáfa birgða fyrir magn af 1 á kostnaði USD 10.00 hver (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 6\. Birgðalokun er framkvæmd. Miðað við vegið meðaltalsaðferð notar kerfið beina uppgjörsaðferð því aðeins ein kvittun er fjárhagslega uppfærð á tímabilinu. Í þessu dæmi er eitt uppgjör búið til á milli 1b og 3b og annað milli 1b og 4b. Engin leiðrétting er gerð vegna þess að hlaupandi meðaltal er það sama og vegið meðaltal.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta með áhrifum þess að velja vegið meðaltal birgðalíkansins og beina uppgjörsregluna án **Taktu með líkamlegt gildi** valmöguleika.

![WeightedAverage DS án Include líkamlegt gildi.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Samantektarjöfnun vegins meðaltals án valkostarins Taka efnislegt virði með

Þegar það eru margar innhreyfingar á tímabili, notar vegið meðaltal samantekna uppgjörsreglu þar sem allar innhreyfingar innan lokatímabils eru teknar saman í færslu sem kallast *vegið meðaltal birgðalokunar*. Allar kvittanir fyrir tímabilið verða jafnaðar á móti útgáfu nýstofnaðrar birgðafærslu. Allar útgáfur tímabilsins verða jafnaðar gegn móttöku nýju birgðafærslunnar. Ef það er eftir birgðaverðmæti eftir birgðalokun, er verðmæti birgðabirgða innifalið í innhreyfingarfærslu vegins meðaltals birgðalokunarfærslur.

Eftirfarandi viðskipti eru sýnd á myndinni sem fylgir:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 7\. Birgðalokun er framkvæmd.
- 7a. Vegið meðaltal fjárhagsútgáfu birgðaloka viðskipta er stofnuð til að leggja saman uppgjör allra birgðafjárhagskvittana.
  - Færsla 1b er gerð upp fyrir magnið 1 með upphæðinni USD 10.00.
  - Færsla 2b er gerð upp fyrir magnið 1 með upphæðinni USD 22.00.
  - Færsla 5b er gerð upp fyrir magnið 1 með upphæðinni USD 30.00.
  - Viðskipti 7a. Er búið til fyrir magnið 3 með uppgjörinu USD 62.00. Þessi færsla vegur á móti summan af þremur kvittunarfærslum sem eru fjárhagslega uppfærðar á tímabilinu.
- 7b. Vegin meðaltal fjárhagsleg innhreyfingar birgðaloka er stofnuð sem mótvægi við fjárhagslega bókaðar útgáfur.
  - Færsla 3b er gerð upp fyrir magnið 1 með upphæðinni USD 20.67. Þessi færsla er leiðrétt með USD 4.67 til að færa upphaflegt gildi USD 16.00 í 20,67 sem er vegið meðaltal fjárhagslegra færslna á tímabilinu.
  - Viðskipti 7b. Er búið til fyrir magnið 1 með uppgjörinu USD 20.67 til að vega upp á móti 3b. Þessi færsla vegur á móti summu einu útgáfufærslunnar sem er fjárhagslega uppfærð á tímabilinu.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta með áhrifum þess að velja vegið meðaltal birgðalíkansins og samantektaruppgjörsregluna án **Taktu með líkamlegt gildi** valmöguleika.

![Vegið meðaltal SS án innihalda líkamlegt gildi.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Bein jöfnun vegins meðaltals með valkostinum Taka efnislegt virði með

Viðfangið **Taktu með líkamlegt gildi** virkar öðruvísi með vegið meðaltal birgðalíkansins en í fyrri útgáfum vörunnar. Þegar þú velur **Taktu með líkamlegt gildi** valkostur fyrir hlut í **Vörulíkanahópur** formi mun kerfið nota líkamlega uppfærðar kvittanir við útreikning á áætlað útgáfukostnaðarverð, eða hlaupandi meðaltal. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Í birgðalokuninni verða aðeins fjárhagslega uppfærðar innhreyfingar hafðar í huga í útreikningi vegins meðaltals.

Eftirfarandi viðskipti eru sýnd á myndinni sem fylgir:

- 1a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 10 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 20,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 15.00 (hlaupandi meðaltal líkamlegra og fjárhagslegra bókaða færslur).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 15.00 (hlaupandi meðaltal líkamlegra og fjárhagslega bókfærðra færslna).
- 4a. Raunveruleg útgáfa birgða fyrir magn sem er 1 á kostnaði USD 15.00 hver (hlaupandi meðaltal líkamlegra og fjárhagslegra færslna).
- 4b. Fjárhagsútgáfa birgða fyrir magn 1 á kostnaði USD 15.00 hver (hlaupandi meðaltal líkamlegra og fjárhagslegra færslna).
- 5a. Raunveruleg útgáfa birgða fyrir magn sem er 1 á kostnaði USD 15.00 hver (hlaupandi meðaltal líkamlegra og fjárhagslegra færslna).
- 6\. Birgðalokun er framkvæmd. Miðað við vegið meðaltalsaðferð notar kerfið beina uppgjörsaðferð því aðeins ein kvittun er fjárhagslega uppfærð á tímabilinu. Í þessu dæmi er eitt uppgjör búið til á milli 1b og 3b og annað milli 1b og 4b. Færslur 3b og 4b eru hvor um sig leiðrétt með USD -5,00 til að færa gildið í USD 10.00.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta með áhrifum þess að velja vegið meðaltal birgðalíkansins og beina uppgjörsregluna með **Taktu með líkamlegt gildi** valmöguleika.

![Vegið meðaltal DS með Include líkamlegt gildi.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Samantektarjöfnun vegins meðaltals með valkostinum Taka efnislegt virði með

The **Taktu með líkamlegt gildi** færibreytan virkar öðruvísi með vegið meðaltal en í fyrri útgáfum. Veldu **Taktu með líkamlegt gildi** gátreit fyrir hlut á **Vörulíkanahópur** síðu. Kerfið mun svo efnislega uppfærðar innhreyfingar þegar áætlað kostnaðarverð eða meðaltal er reiknað út. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Í birgðalokuninni verða aðeins fjárhagslega uppfærðar innhreyfingar hafðar í huga í útreikningi vegins meðaltals. Við mælum með mánaðarlegri birgðalokun þegar notað er birgðalíkanið með vegið meðaltal. Í þessu dæmi um samantektarjöfnun á vegnu meðaltali, er birgðalíkanið merkt til að innihalda efnislega virðið.

Eftirfarandi viðskipti eru sýnd á myndinni sem fylgir:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal líkamlegra og fjárhagslegra bókaða færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal líkamlegra og fjárhagslegra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.67 (hlaupandi meðaltal líkamlegra og fjárhagslega bókfærðra færslna).
- 7\. Birgðalokun er framkvæmd.
- 7a. Vegið meðaltal fjárhagsútgáfu birgðaloka viðskipta er stofnuð til að leggja saman uppgjör allra birgðafjárhagskvittana.
  - Færsla 1b er gerð upp fyrir magnið 1 með upphæðinni USD 10.00.
  - Færsla 2b er gerð upp fyrir magnið 1 með upphæðinni USD 22.00.
  - Færsla 5b er gerð upp fyrir magnið 1 með upphæðinni USD 30.00.
  - Viðskipti 7a. Er búið til fyrir magnið 3 með uppgjörinu USD 62.00.  
- 7b. Vegin meðaltal fjárhagsleg innhreyfingar birgðaloka er stofnuð sem mótvægi fyrir fjárhagslega lokuðum útgáfufærslum.
  - Færsla 3b er gerð upp fyrir magnið 1 með upphæðinni USD 20.67. Þessi færsla er leiðrétt með USD 4.67 til að færa upphaflegt gildi USD 16.00 í 20,67 sem er vegið meðaltal fjárhagslegra færslna á tímabilinu.
  - Viðskipti 7b. Er búið til fyrir magnið 1 með uppgjörinu USD 20.67 til að vega upp á móti 3b.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta með áhrifum þess að velja vegið meðaltal birgðalíkansins og samantektaruppgjörsregluna án **Taktu með líkamlegt gildi** valmöguleika.

![WeightedAverage SS með Include líkamlegt gildi.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-with-marking"></a>Vegið meðaltal með merkingu

Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar ætlunin er að ganga úr skugga um nákvæman kostnað við birgðir þegar færsla er bókuð eða þegar birgðalokun er framkvæmd.

Þjónustudeild fyrir viðskiptavini, hefur til dæmis fengið flýtipöntun frá mikilvægum viðskiptavini. Vegna þess að þetta er flýtipöntun þarftu að borga meira fyrir þennan hlut til að sinna beiðni viðskiptavinarins. Þú verður að vera viss um að kostnaður þessa birgðavara endurspeglast í framlegðinni, eða kostnaður seldra vara (COGS), fyrir þessa sölupöntunarreikning.

Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Til dæmis, þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður. Síðan er kostnaður seldra VARA 120,00 USD í staðinn fyrir núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði.

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra.

Innhreyfingarfærsla er merkt við úthreyfingarfærslu. Þá verður matsaðferðin sem valin er fyrir vörulíkanaflokk vörunnar hunsuð og kerfið jafnar þessar færslur hver við annan.

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þetta frá sölupöntunarlínu á síðunni **Ítarupplýsingar sölupöntunar**. Opnu kvittunarfærslurnar eru sýndar á **Merking** síðu.

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók.

Eftirfarandi viðskipti eru sýnd á myndinni sem fylgir:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3c. Fjárhagsútgáfa birgða fyrir 3b er merkt við birgðafjárútgáfu fyrir 2b.
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 7\. Birgðalokun er framkvæmd. Á grundvelli merkingarreglunnar sem notar vegið meðaltalsaðferð eru mörkuðu færslurnar jafnaðar hver á móti öðrum. Í þessu dæmi er 3b jafnað á móti 2b og leiðrétting fyrir USD 6.00 er sett á 3b til að færa gildið í USD 22.00. Í þessu dæmi eru engar viðbótaruppgjörir gerðar vegna þess að lokun stofnar aðeins uppgjör fyrir fjárhagslega uppfærðar færslur.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta með áhrifum þess að velja vegið meðaltal birgðalíkansins með merkingu.

![Vegið meðaltal með Merkingu.](media/weighted-average-with-marking.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
