---
title: Vegin meðaldagsetning með innihalda líkamlegt gildi og merkingu
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672123"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Vegin meðaldagsetning með innihalda líkamlegt gildi og merkingu

[!include [banner](../includes/banner.md)]

*Vegin meðaldagsetning* er birgðalíkan sem byggir á meðaltali sem er reiknað með því að margfalda hvern þátt (vöruviðskipti) með stuðli (kostnaðarverði) sem endurspeglar mikilvægi hans (magn) á hverjum degi á tímabilinu. Með öðrum orðum, þetta birgðalíkan úthlutar kostnaði við útgáfufærslur út frá meðalgildi allra birgða sem berast á hverjum degi, að viðbættum birgðum á lager frá fyrri degi.

Þegar þú keyrir birgðalokun með því að nota vegið meðaltal dagsetningar birgðalíkansins, er hægt að nota tvær aðferðir til að stofna uppgjör. Venjulega eru allar kvittanir jafnaðar á móti sýndarútgáfu sem geymir heildarmóttekið magn og gildi. Þetta sýndarmál er með samsvarandi sýndarkvittun sem málin eru gerð upp frá. Þannig fá öll blöð sama meðalkostnað á hverjum degi. Sýndarútgáfan og sýndarkvittunin geta talist sýndarflutningur. Þessi sýndarflutningur er nefndur *vegið meðaltal birgðalokunarflutnings*. Þess vegna er þessi uppgjörsaðferð þekkt sem a *vegið meðaltal yfirlits uppgjörs*. Ef það er aðeins ein kvittun er hægt að gera upp öll mál út frá henni og enginn sýndarflutningur verður til. Þessi uppgjörsaðferð er nefnd *beint uppgjör*. Allar birgðir sem eru til staðar eftir að birgðalokun er framkvæmd eru metnar á vegið meðaltal frá síðasta degi fyrra tímabils og innifalið í útreikningi vegins meðaltals dagsetningar á næsta tímabili.

Hægt er að hnekkja meginreglunni um vegið meðaltal dagsetningar með því að merkja birgðafærslur þannig að tiltekin vörumóttaka sé jöfnuð á móti tiltekinni útgáfu. Reglubundin birgðalokun er nauðsynleg þegar þú notar vegið meðaltal dagsetningar birgðalíkansins til að stofna uppgjör og leiðrétta verðmæti útgáfur í samræmi við dagsetningarregluna fyrir vegið meðaltal. Þar til þú keyrir birgðalokunina eru útgáfufærslur metnar á hlaupandi meðaltali þegar líkamlegar og fjárhagslegar uppfærslur áttu sér stað. Nema þú sért að nota merkingu er hlaupandi meðaltal reiknað út þegar líkamleg eða fjárhagsleg uppfærsla er framkvæmd.

Vegið meðaltal birgðakostnaðaraðferðar er reiknað út með því að nota eftirfarandi formúlu á hverjum degi:

*Kostnaður* = \[ (*Q*<sub>*b*</sub> ×*P*<sub>*b*</sub>) +&#x2211;<sub>*n*</sub> (*Q*<sub>*n*</sub> ×*P*<sub>*n*</sub>)\] ÷ (*Q*<sub>*b*</sub> +&#x2211;<sub>*n*</sub>*Q*<sub>*n*</sub>)

- *Q* = Magn viðskipta
- *P* = Verð viðskipta

Með öðrum orðum, veginn meðalkostnaður jafngildir upphafsmagni sinnum upphafsverði, að viðbættum summu hvers innhreyfingarmagns sinnum innhreyfingarverði, öllu deilt með upphafsmagni plús summan af innhreyfingarmagni.

Við lokun birgða er útreikningurinn framkvæmdur á hverjum degi á lokunartímabilinu.

> [!NOTE]
> Sjá nánar um byggðir [Birgðalokun](inventory-close.md).

Eftirfarandi dæmi sýna áhrif þess að nota vegið meðaltalsdagsetningu með fimm stillingum:

- Bein jöfnun vegins meðaltals dagsetningar án valkostarins **Taka efnislegt virði með**
- Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins **Taka efnislegt virði með**
- Bein jöfnun vegins meðaltals dagsetningar með valkostinum **Taka efnislegt virði með**
- Samantektarjöfnun vegins meðaltals dagsetningar með valkostinum **Taka efnislegt virði með**
- Vegið meðaltal dagsetningar með merkingu

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Bein jöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með

Reglan um bein uppgjör stofnar uppgjör beint á milli innhreyfinga og útgáfu, án þess að stofna viðbótarbirgðafærslur. Kerfið notar þessa beinu uppgjörsreglu við eftirfarandi aðstæður:

- Ein kvittun og eitt eða fleiri tölublöð hafa verið bókuð á tímabilinu.
- Einungis úthreyfingar hafa verið bókaðar á tímabilinu og birgðir innihalda vörur á lager frá fyrri lokun.

Í þessu dæmi er **Taktu með líkamlegt gildi** gátreiturinn er hreinsaður á **Vörulíkanahópur** síðu fyrir útgefna vöruna. Skýringarmyndin sem fylgir sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 10 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 20,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 10.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 10.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Fjárhagsútgáfa birgða fyrir magn 1 á kostnaði USD 20.00 hver (hlaupandi meðaltal fjárhagslega bókfærðra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd. Miðað við dagsetningaraðferðina fyrir vegið meðaltal notar kerfið beina uppgjörsaðferð fyrir 30. desember (30.12.) vegna þess að aðeins ein kvittun er fjárhagslega uppfærð þann 30.12. Í þessu dæmi er ein uppgjör búin til á milli færslu 1b og 3b. Leiðrétting á USD 10.00 er gerð til að færa verðmæti færslu 3b upp í 20.00. Engin leiðrétting eða uppgjör er gert 31. desember (31.12.) vegna þess að engin fjárhagslega uppfærð mál eru 31.12.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta og áhrif þess að nota vegið meðaltal birgðalíkansins og beina uppgjörsregluna án **Taktu með líkamlegt gildi** valmöguleika.

![Bein jöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Lykill að skýringarmyndinni:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með þunnum svörtum lóðréttum línum. Dagsetningarnar eru skráðar neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðum lóðréttum strikalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með

Þegar það eru margar innhreyfingar á einu tímabili notar vegin meðaltalsdagsetning samantekna uppgjörsreglu, þar sem allar innhreyfingar á einum degi eru teknar saman í færslu sem er nefnd *vegið meðaltal birgðalokunar*. Allar kvittanir dagsins verða jafnaðar á móti útgáfu nýstofnaðrar birgðafærslu. Öll mál dagsins verða gerð upp gegn móttöku nýju birgðafærslunnar. Ef það er eftir birgðaverðmæti eftir birgðalokun, er birgðaverðmæti birgða innifalið í innhreyfingarfærslu vegins meðaltals birgðalokunarfærslur.

Skýringarmyndin sem fylgir sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd.
- 7a. Vegið meðaltal fjárhagsútgáfu birgðaloka viðskipta er stofnuð til að leggja saman uppgjör allra birgðafjárhagskvittana.

    - Færsla 1b er gerð upp fyrir magnið 1 með uppgjörnu magni USD 10.00.
    - Færsla 2b er gerð upp fyrir magnið 1 með uppgert magn af USD 22.00.
    - Færsla 7a er búin til fyrir magnið 2 með uppgert magn af USD 32.00. Þessi færsla vegur á móti summan af tveimur kvittunarfærslum sem eru fjárhagslega uppfærðar á tímabilinu.

- 7b. Vegin meðaltal fjárhagsleg innhreyfingar birgðaloka er stofnuð sem mótvægi fyrir fjárhagslega bókaðar útgáfur.

    - Færsla 3b er gerð upp fyrir magnið 1 með uppgert magn af USD 16.00. Þessi færsla er ekki leiðrétt vegna þess að hún er vegið meðaltal fjárhagslegra færslna 1. desember (12/1).
    - Færsla 7b er búin til fyrir magnið 2 með fjárhagsupphæðinni USD 32.00 og uppgjörnu upphæðinni USD 16.00 til að vega upp á móti færslu 3b. Þessi færsla vegur á móti summu einu útgáfufærslunnar sem er fjárhagslega uppfærð á tímabilinu. Viðskiptin eru enn opin vegna þess að það er enn einn á hendi.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta og áhrif þess að nota vegið meðaltal birgðalíkansins og samantekna uppgjörsreglu, en án þess að nota **Taktu með líkamlegt gildi** valmöguleika.

![Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Lykill að skýringarmyndinni:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með þunnum svörtum lóðréttum línum. Dagsetningarnar eru skráðar neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðum lóðréttum strikalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Bein jöfnun vegins meðaltals dagsetningar með valkostinum Taka efnislegt virði með

Í núverandi útgáfu vörunnar er **Taktu með líkamlegt gildi** valmöguleikinn virkar öðruvísi með vegið meðaltal dagsetningar birgðalíkansins en það virkaði í fyrri útgáfum. Þegar þú velur **Taktu með líkamlegt gildi** gátreit fyrir hlut á **Vörulíkanahópur** síðu mun kerfið nota líkamlega uppfærðar kvittanir þegar það reiknar út áætlað útgáfukostnaðarverð eða hlaupandi meðaltal. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Við birgðalokun eru aðeins innhreyfingar sem hafa verið fjárhagslega uppfærðar teknar með í útreikning á vegnu meðaltali.

Skýringarmyndin sem fylgir sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 10 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 10 með kostnaðinn 20,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 15.00 (hlaupandi meðaltal líkamlegra og fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 15.00 (hlaupandi meðaltal líkamlegra og fjárhagslega bókfærðra færslna).

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magn af 1 á kostnaði USD 21.25 hver (hlaupandi meðaltal líkamlegra og fjárhagslegra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd. Miðað við dagsetningaraðferðina fyrir vegið meðaltal notar kerfið beina uppgjörsaðferð fyrir 30. desember (30.12.) vegna þess að aðeins ein kvittun er fjárhagslega uppfærð þann 30.12. Í þessu dæmi er ein uppgjör búin til á milli færslu 1b og 3b. Engin leiðrétting er gerð á málaflokknum 30.12. Að auki er engin leiðrétting eða uppgjör gerð 31. desember (31.12.) vegna þess að engin fjárhagslega uppfærð mál eru 31.12.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta og áhrif þess að nota vegið meðaltal birgðalíkansins og beina uppgjörsregluna með **Taktu með líkamlegt gildi** valmöguleika.

![Vegið meðaltal beint uppgjörs með Include efnisvirði.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Lykill að skýringarmyndinni:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með þunnum svörtum lóðréttum línum. Dagsetningarnar eru skráðar neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðum lóðréttum strikalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með

Í núverandi útgáfu vörunnar er **Taktu með líkamlegt gildi** valmöguleikinn virkar öðruvísi með vegið meðaltal en það virkaði í fyrri útgáfum. Þegar þú velur **Taktu með líkamlegt gildi** gátreit fyrir hlut á **Vörulíkanahópur** síðu mun kerfið nota líkamlega uppfærðar kvittanir þegar það reiknar út áætlað kostnaðarverð, eða hlaupandi meðaltal. Úthreyfingar verða bókaðar á grundvelli þessa áætlaða kostnaðarverðs á tímabilinu. Við birgðalokun eru aðeins innhreyfingar sem hafa verið fjárhagslega uppfærðar teknar með í útreikning á vegnu meðaltali. Við mælum með að þú framkvæmir mánaðarlega birgðalokun þegar þú notar vegið meðaltal birgðalíkansins. Í þessu dæmi um vegið meðaltal dagsetningar samantektaruppgjörs er birgðalíkanið merkt til að innihalda efnislegt gildi.

Skýringarmyndin sem fylgir sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magn sem er 1 á kostnaðarverði USD 16.00 (hlaupandi meðaltal af líkamlegum og fjárhagslegum bókuðum færslum).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal líkamlegra og fjárhagslegra bókaða færslna).

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.67 (hlaupandi meðaltal líkamlegra og fjárhagslegra bókaða færslur).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd.
- 7a. Vegið meðaltal fjárhagsútgáfu birgðaloka viðskipta er stofnuð til að leggja saman uppgjör allra birgðafjárhagskvittana.

    - Færsla 1b er gerð upp fyrir magnið 1 með uppgjörnu magni USD 10.00.
    - Færsla 2b er gerð upp fyrir magnið 1 með uppgert magn af USD 22.00.
    - Færsla 7a er búin til fyrir magnið 2 með uppgert magn af USD 32.00. Þessi færsla vegur á móti summan af tveimur kvittunarfærslum sem eru fjárhagslega uppfærðar á tímabilinu.

- 7b. Vegin meðaltal fjárhagsleg innhreyfingar birgðaloka er stofnuð sem mótvægi fyrir fjárhagslega bókaðar útgáfur.

    - Færsla 3b er gerð upp fyrir magnið 1 með uppgert magn af USD 16.00. Þessi færsla er ekki leiðrétt vegna þess að hún er vegið meðaltal fjárhagslegra færslna 1. desember (12/1).
    - Færsla 7b er búin til fyrir magnið 2 með fjárhagsupphæðinni USD 32.00 og uppgjörnu upphæðinni USD 16.00 til að vega upp á móti færslu 3b. Þessi færsla vegur á móti summu einu útgáfufærslunnar sem er fjárhagslega uppfærð á tímabilinu. Viðskiptin eru enn opin vegna þess að það er enn einn á hendi.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta og áhrif þess að nota vegið meðaltal birgðalíkansins og samantekna uppgjörsreglu án **Taktu með líkamlegt gildi** valmöguleika.

![Vegið meðaltal yfirlits uppgjörs með Include efnislegt gildi.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Lykill að skýringarmyndinni:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með þunnum svörtum lóðréttum línum. Dagsetningarnar eru skráðar neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðum lóðréttum strikalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-when-marking-is-used"></a>Vegið meðaltal dagsetningar með merkingu

Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Þú getur notað merkingu þegar þú vilt ganga úr skugga um nákvæmlega kostnað birgða þegar færslan er bókuð eða birgðalokun er framkvæmd.

Þjónustudeild fyrir viðskiptavini, hefur til dæmis fengið flýtipöntun frá mikilvægum viðskiptavini. Vegna þess að þetta er flýtipöntun þarftu að borga meira fyrir þennan hlut til að sinna beiðni viðskiptavinarins. Þú verður að vera viss um að kostnaður þessarar birgðavöru endurspeglast í framlegð, eða kostnaði við seldar vörur (COGS), fyrir þennan sölupöntunarreikning.

Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef sölupöntunarskjalið er merkt við innkaupapöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, verða COGS USD 120.00 í stað núverandi meðalkostnaðar vörunnar. Ef merking á sér stað eftir að fylgiseðill sölupöntunar eða reikningur hefur verið bókaður, verður COGS bókað á hlaupandi meðalkostnaðarverði.

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra.

Ef kvittunarfærsla er merkt við útgáfufærslu verður matsaðferðin sem valin er fyrir vörulíkanaflokk vörunnar hunsuð og kerfið jafnar þessar færslur hver við annan.

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Þú getur gert þessa merkingu úr sölupöntunarlínu á **Upplýsingar um sölupöntun** síðu. Opnu kvittunarfærslurnar eru sýndar á **Merking** síðu.

Einnig er Hægt að merkja úthreyfingarfærslu við innhreyfingu eftir að færslan er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók.

Skýringarmyndin sem fylgir sýnir þessar færslur:

**Dagur 1:**

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3c. Fjárhagsútgáfa birgða fyrir færslu 3b er merkt við birgðafjárútgáfu fyrir færslu 2b.

**Dagur 2:**

- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).

**Dagur 3:**

- 7\. Birgðalokun er framkvæmd. Á grundvelli merkingarreglunnar sem notar vegið meðaltalsaðferð eru mörkuðu færslurnar jafnaðar hver á móti öðrum. Í þessu dæmi er færslu 3b jöfnuð á móti færslu 2b og leiðrétting fyrir USD 6.00 er bókuð á færslu 3b til að færa gildið í USD 22.00. Í þessu dæmi eru engar viðbótaruppgjörir gerðar vegna þess að lokun stofnar aðeins uppgjör fyrir fjárhagslega uppfærðar færslur.

Eftirfarandi skýringarmynd sýnir þessa röð viðskipta og áhrif þess að nota vegið meðaltal birgðalíkansins með merkingu.

![Vegið meðaltal með merkingu.](media/weighted-average-date-with-marking.png)

**Lykill að skýringarmyndinni:**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Dagsetningar eru aðskildar með þunnum svörtum lóðréttum línum. Dagsetningarnar eru skráðar neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðum lóðréttum strikalínum.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
