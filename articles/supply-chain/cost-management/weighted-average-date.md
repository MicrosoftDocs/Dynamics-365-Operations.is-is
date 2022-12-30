---
title: Dagsetning vegins meðaltals með Taka efnislegt virði með og merkingu
description: Dagsetning vegins meðaltals er birgðalíkan byggt á reglunni um vegið meðaltal þar sem innhreyfingar úr birgðum eru metnar á meðaltalsgildi vara sem tekið er á móti í birgðum fyrir hvern einstakan dag á birgðalokunartímabilinu.
author: JennySong-SH
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1497cb08f4cc5a455c832b9bf125c309cd90aa3d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672123"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Dagsetning vegins meðaltals með Taka efnislegt virði með og merkingu

[!include [banner](../includes/banner.md)]

*Dagsetning vegins meðaltals* er birgðalíkan sem byggir á meðaltali sem er reiknað með því að margfalda hverja einingu (vörufærslu) með þætti (kostnaðarverði) sem endurspeglar mikilvægi hans (magn) á hverjum degi á tímabilinu. Þetta birgðalíkan sýnir með öðrum orðum kostnað við úthreyfingarfærslur miðað við meðalvirði allra birgða sem eru mótteknar á hverjum degi og allar birgðir á lager frá deginum áður.

Þegar þú keyrir birgðalokun með því að nota birgðalíkan vegins meðaltals er hægt að nota tvær aðferðir til að búa til jöfnun. Yfirleitt eru allar innhreyfingar jafnaðar á móti sýndarúthreyfingu sem geymir heildarmagn og virði móttekins magns. Þessi sýndarúthreyfing hefur samsvarandi sýndarinnhreyfingu þaðan sem úthreyfingar eru jafnaðar. Þannig fá allar úthreyfingar sama meðalkostnað á hverjum degi. Sýndarúthreyfingu og -innhreyfingu er hægt að sjá sem sýndarflutning. Þessi sýndarflutningur er nefndur *birgðalokunarfærsla með vegnu meðaltali*. Þess vegna er þessi jöfnunaraðferð þekkt sem *Samantektarjöfnun vegins meðaltals*. Ef aðeins er um að ræða innhreyfingu er hægt að jafna allar úthreyfingar þaðan og sýndarfærslan verður ekki stofnuð. Þessi jöfnunaraðferð er kölluð *bein jöfnunaraðferð*. Allar birgðir sem eru á lager eftir birgðalokun eru metnar sem vegið meðaltal frá síðasta degi fyrra tímabils og teknar með í útreikningi vegins meðaltals á næsta tímabili.

Hægt er að hnekkja reglunni um dagsetning vegins meðaltals með því að merkja birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu. Reglubundin birgðalokun er nauðsynleg þegar notað er birgðalíkan vegins meðaltals til að búa til uppgjör og breyta gildi úthreyfinga í samræmi við dagsetningarreglu vegins meðaltals. Þar til þú keyrir birgðalokun, eru úthreyfingarfærslur metnar á hlaupandi meðaltali þegar efnislegar og fjárhagslegar uppfærslur áttu sér stað. Nema ef merking er notuð þá er hlaupandi meðaltal reiknað út þegar efnisleg eða fjárhagsleg uppfærsla er framkvæmd.

Vegið meðaltal dagsetningar aðferðar kostnaðarútreiknings er reiknuð út með eftirfarandi formúlu á hverjum degi:

*Kostnaður* = \[(*Q*<sub>*b*</sub> × *P*<sub>*b*</sub>) + &#x2211;<sub>*n*</sub>(*Q*<sub>*n*</sub> × *P*<sub>*n*</sub>)\] ÷ (*Q*<sub>*b*</sub> + &#x2211;<sub>*n*</sub>*Q*<sub>*n*</sub>)

- *Q* = Magn færslu
- *P* = Verð færslunnar

Með öðrum orðum, kostnaður vegið meðaltal jafngildir upphafsmagni sinnum upphafsverð, að viðbættri samtölu hvers móttekins magns sinnum upphafsverð þess, allt deilt með upphafsmagni auk samtölu móttekins magns.

Við birgðalokun er útreikningur framkvæmdur á hverjum degi í lokunartímabilinu.

> [!NOTE]
> Frekari upplýsingar um jöfnun er að finna í [Birgðalokun](inventory-close.md).

Eftirfarandi dæmi skýra áhrif þess að nota vegna meðaltalsdagsetningu með fimm ólíkum skilgreiningum:

- Bein jöfnun vegins meðaltals dagsetningar án valkostarins **Taka efnislegt virði með**
- Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins **Taka efnislegt virði með**
- Bein jöfnun vegins meðaltals dagsetningar með valkostinum **Taka efnislegt virði með**
- Samantektarjöfnun vegins meðaltals dagsetningar með valkostinum **Taka efnislegt virði með**
- Vegið meðaltal dagsetningar með merkingu

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Bein jöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með

Reglan um beina jöfnun býr til jafnanir beint á milli innhreyfing og úthreyfinga, án þess að búa til viðbótarbirgðafærslur. Kerfið notar þessa reglu beinnar jöfnunar í eftirfarandi aðstæðum:

- Ein innhreyfing og eitt eða fleiri vandamál hafa verið bókaðar á þessu tímabili.
- Einungis úthreyfingar hafa verið bókaðar á tímabilinu og birgðir innihalda vörur á lager frá fyrri lokun.

Í þessu dæmi er gátreiturinn **Taka efnislegt virði með** hreinsaður á síðu fyrir **Vörulíkanaflokkur** fyrir vöruna sem er losuð. Eftirfarandi skýringarmynd sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 10 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 20,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 10,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 10,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 20,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd. Samkvæmt dagsetningaraðferð vegins meðaltals notar kerfið beina jöfnunaraðferð fyrir 30. desember (30/12) vegna þess að aðeins ein innhreyfing er uppfærð fjárhagslega þann 30/12. Í þessu dæmi er búið til eitt uppgjör milli færslna 1b og 3b. Leiðrétting upp á USD 10,00 er gerð til að færa virði færslu 3b upp í USD 20,00. Engin leiðrétting eða uppgjör á sér stað 31. desember (31/12) vegna þess að það eru engin fjárhagslega uppfærðar úthreyfingar þann 31/12.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum án áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun með valkosti **Hafa með efnislegt virði**.

![Bein jöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Lykill að skýringarmynd:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með mjóum, svörtum lóðréttum línum. Dagsetningarnar eru sýndar neðst á skýringarmyndinni.
- Birgðalokun eru sýndar með rauðum, lóðréttum brotalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með

Þegar margar innhreyfingar eru á tilteknu tímabili notar vegið meðaltal samantektarjöfnunarregluna, þar sem allar innhreyfingar á einum degi eru teknar saman í færslu sem er nefnd *vegið meðaltal birgðalokunar*. Öll innhreyfing dagsins verður gerð upp gegn úthreyfingu nýrra birgðafærslna. Öll úthreyfing dagsins verður gerð upp gegn innhreyfingu nýrra birgðafærslna. Ef birgðavirði er eftir á lager eftir birgðalokun er birgðavirði á lager innifalið í innhreyfingarfærslu í vegnu meðaltali birgðalokunarfærslna.

Eftirfarandi skýringarmynd sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 16,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 23,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd.
- 7a. Fjárhagslega úthreyfingin Birgðalokunarfærsla vegins meðaltals er stofnuð til að leggja saman jafnanir allra fjárhagslegu innhreyfinga birgðanna.

    - Færsla 1b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 10,00 USD.
    - Færsla 2b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 22,00 USD.
    - Færsla 7a er jöfnuð fyrir magnið 2 með jöfnuðu upphæðina 32,00 USD. Þessi færsla vegur upp á móti summu einnar útgáfufærslu sem er uppfærð fjárhagslega á tímabilinu.

- 7b. Fjárhagslega innhreyfingin Birgðalokunarfærsla vegins meðaltals er stofnuð sem mótvægi við fjárhagslega bókaðar innhreyfingar.

    - Færsla 3b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 16,00 USD. Þessi færsla er ekki leiðrétt vegna þess að hún er vegið meðaltal fjárhagslegra bókaðra færslna 1. desember (1/12).
    - Færsla 7b er stofnuð fyrir upphæðina 2 með fjáhagslegu upphæðinni 32,00 USD og jafnaðri upphæðinni 16,00 USD til að vega upp á móti færslu 3b. Þessi færsla vegur upp á móti summu einnar útgáfufærslu sem er uppfærð fjárhagslega á tímabilinu. Færslan er áfram opin vegna þess að það er áfram ein á lager.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun án valkostarins **Taka efnislegt virði með**.

![Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Lykill að skýringarmynd:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með mjóum, svörtum lóðréttum línum. Dagsetningarnar eru sýndar neðst á skýringarmyndinni.
- Birgðalokun eru sýndar með rauðum, lóðréttum brotalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Bein jöfnun vegins meðaltals dagsetningar með valkostinum Taka efnislegt virði með

Í núverandi útgáfu vörunnar virkar valkosturinn **Taka með efnislegt virði** öðruvísi með birgðalíkani vegins meðaltals en í fyrri útgáfum. Ef gátreiturinn **Efnislegt virði tekið með** er valinn fyrir vöru á síðunni **Vörulíkanaflokkur** notar kerfið efnislega uppfærðar innhreyfingar þegar það reiknar út áætlað útgefið kostnaðarverð eða meðaltal. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Við birgðalokun eru aðeins innhreyfingar sem hafa verið fjárhagslega uppfærðar teknar með í útreikning á vegnu meðaltali.

Eftirfarandi skýringarmynd sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 10 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 20,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 15,00 USD (hlaupandi meðaltal fjárhagslega og efnislegra bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 15,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 21,25 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd. Samkvæmt dagsetningaraðferð vegins meðaltals notar kerfið beina jöfnunaraðferð fyrir 30. desember (30/12) vegna þess að aðeins ein innhreyfing er uppfærð fjárhagslega þann 30/12. Í þessu dæmi er búið til eitt uppgjör milli færslna 1b og 3b. Engin leiðrétting er gerð á vandamálinu þann 12/30. Þar að auki er engin leiðrétting eða uppgjör 31. desember (31/12) vegna þess að það eru engin fjárhagslega uppfærðar úthreyfingar þann 31/12.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun með valkosti **Hafa með efnislegt virði**.

![Bein jöfnun vegins meðaltals með valkostinum Taka efnislegt virði með.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Lykill að skýringarmynd:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með mjóum, svörtum lóðréttum línum. Dagsetningarnar eru sýndar neðst á skýringarmyndinni.
- Birgðalokun eru sýndar með rauðum, lóðréttum brotalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með

Í núverandi útgáfu vörunnar virkar valkosturinn **Taka með efnislegt virði** öðruvísi með vegið meðaltal en í fyrri útgáfum. Ef gátreiturinn **Efnislegt virði tekið með** er valinn fyrir vöru á síðunni **Vörulíkanaflokkur** notar kerfið efnislega uppfærðar innhreyfingar þegar það reiknar út áætlað kostnaðarverð eða meðaltal. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Við birgðalokun eru aðeins innhreyfingar sem hafa verið fjárhagslega uppfærðar teknar með í útreikning á vegnu meðaltali. Við mælum með mánaðarlegri birgðalokun þegar notað er birgðalíkan vegins meðaltals. Í þessu dæmi samantektarjöfnunar á vegnu meðaltali, er birgðalíkanið merkt til að innihalda efnislega virðið.

Eftirfarandi skýringarmynd sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD (hlaupandi meðaltal fjárhagslega og efnislegra bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 23,67 USD (hlaupandi meðaltal fjárhagslega og efnislegra bókaðra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd.
- 7a. Fjárhagslega úthreyfingin Birgðalokunarfærsla vegins meðaltals er stofnuð til að leggja saman jafnanir allra fjárhagslegu innhreyfinga birgðanna.

    - Færsla 1b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 10,00 USD.
    - Færsla 2b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 22,00 USD.
    - Færsla 7a er jöfnuð fyrir magnið 2 með jöfnuðu upphæðina 32,00 USD. Þessi færsla vegur upp á móti summu einnar útgáfufærslu sem er uppfærð fjárhagslega á tímabilinu.

- 7b. Fjárhagslega innhreyfingin Birgðalokunarfærsla vegins meðaltals er stofnuð sem mótvægi við fjárhagslega bókaðar innhreyfingar.

    - Færsla 3b er jöfnuð fyrir magnið 1 með jöfnuðu upphæðina 16,00 USD. Þessi færsla er ekki leiðrétt vegna þess að hún er vegið meðaltal fjárhagslegra bókaðra færslna 1. desember (1/12).
    - Færsla 7b er stofnuð fyrir upphæðina 2 með fjáhagslegu upphæðinni 32,00 USD og jafnaðri upphæðinni 16,00 USD til að vega upp á móti færslu 3b. Þessi færsla vegur upp á móti summu einnar útgáfufærslu sem er uppfærð fjárhagslega á tímabilinu. Færslan er áfram opin vegna þess að það er áfram ein á lager.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum án áhrifunum af því að velja birgðalíkan vegins meðaltals og samantekt regluna um beina jöfnun með valkosti **Hafa með efnislegt virði**.

![Jöfnun vegins meðaltals með valkostinum Taka efnislegt virði með.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Lykill að skýringarmynd:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með mjóum, svörtum lóðréttum línum. Dagsetningarnar eru sýndar neðst á skýringarmyndinni.
- Birgðalokun eru sýndar með rauðum, lóðréttum brotalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-when-marking-is-used"></a>Vegið meðaltal dagsetningar með merkingu

Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar ætlunin er að ganga úr skugga um nákvæman kostnað við birgðir þegar færsla er bókuð eða þegar birgðalokun er framkvæmd.

Þjónustudeild fyrir viðskiptavini, hefur til dæmis fengið flýtipöntun frá mikilvægum viðskiptavini. Þar sem þetta er flýtipöntun þarf að greiða meira fyrir vöruna til þess að geta mætt beiðni viðskiptavinarins. Þá er nauðsynlegt að vera viss um að kostnaðurinn við þessa birgðavöru endurspeglist í framlegð, eða kostnaði seldra vara (COGS) á þessum sölupöntunarreikningi.

Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef sölupöntunarskjal er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, er kostnaður seldra VARA 120,00 USD, en ekki núverandi meðaltal kostnaðar vörunnar. Ef merking á sér stað áður en að fylgiseðill sölupöntunarinnar eða reikningur er bókaður, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði.

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra.

Þegar innhreyfingarfærsla er merkt úthreyfingarfærslu, er matsaðferðin sem valin er fyrir birgðalíkanaflokk vörunnar hunsaður og kerfið mun jafna þessar færslur hvor við aðra.

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þessa merkingu frá sölupöntunarlínu á síðunni **Ítarupplýsingar sölupöntunar**. Opnar innhreyfingarfærslur eru skoðaðar á síðunni **Merking**.

Einnig er Hægt að merkja úthreyfingarfærslu við innhreyfingu eftir að færslan er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók.

Eftirfarandi skýringarmynd sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 16,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3c. Fjárhagsleg úthreyfing birgða 3b er merkt við fjárhagsleg úthreyfing birgða fyrir færslu 2b.

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 23,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd. Samkvæmt merkingarreglunni sem notar aðferðina vegið meðaltal eru merktu færslurnar jafnaðar á móti hvor annarri. Í þessu dæmi er færsla 3b gerð upp á móti færslu 2b og leiðrétting fyrir 6,00 USD er sett inn á færslu 3b til að færa gildið í 22,00 USD. Í þessu dæmi eru engin viðbótarjafnanir gerð vegna þess að lokunin skapar einungis jafnanir fyrir fjárhagslega uppfærðar færslur.

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum og áhrifunum af því að velja birgðalíkan vegins meðaltals ásamt merkingum.

![Vegið meðaltal með merkingu.](media/weighted-average-date-with-marking.png)

**Lykill að skýringarmynd:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með mjóum, svörtum lóðréttum línum. Dagsetningarnar eru sýndar neðst á skýringarmyndinni.
- Birgðalokun eru sýndar með rauðum, lóðréttum brotalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
