---
title: Sjóðstreymisspár
description: Þetta efnisatriði gefur yfirlit yfir ferli sjóðstreymisspár. Það útskýrir einnig hvernig sjóðstreymisspá er samþætt við aðrar einingar í kerfinu.
author: saraschi2
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 681817f2879034d65b53666a9d56ec00cc175ad8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "324492"
---
# <a name="cash-flow-forecasting"></a>Sjóðstreymisspár

[!include [banner](../includes/banner.md)]

Hægt er að nota verkfæri fyrir sjóðstreymisspár til að greina væntanlegt sjóðstreymi og gjaldeyrisþörf þannig að hægt sé að meta framtíðarþörf fyrirtækis fyrir lausafé. Til að gera spá um sjóðstreymi þarf fyrst að gera eftirfarandi:

- Greina og fá lista yfir alla greiðslugetulykla. Greiðslugetulyklar eru lausafjárreikningar fyrirtækis eða jafngildi þeirra.
- Skilgreina virkni spáa á færslum sem hafa áhrif á greiðslugetulykla fyrirtækisins.

Þegar þessu er lokið er hægt að reikna og greina sjóðstreymisspár og væntanlega gjaldeyrisþörf.

## <a name="cash-flow-forecasting-integration"></a>Samþætting á sjóðstreymisspám

Hægt er að samþætta sjóðstreymisspár við fjárhag, viðskiptaskuldir, viðskiptakröfur, fjárhagsáætlun og birgðastjórnun. Spáferlið notast við færsluupplýsingar sem eru skráðar í kerfið og útreikningarnir spá fyrir um væntanleg áhrif hverrar færslu á lausafé. Eftirfarandi færslur eru teknar með í reikninginn við útreikninga á sjóðstreymi:

- **Sölupantanir** – Sölupantanir sem ekki hafa verið reikningsfærðar og verða að efnislegri eða fjárhagslegri sölu.
- **Innkaupapantanir** – Innkaupapantanir sem ekki hafa verið reikningsfærðar og verða að efnislegum eða fjárhagslegum innkaupum.
- **Viðskiptakröfur** – Opnar viðskiptamannafærslur (reikninga sem hafa ekki verið greiddir).
- **Viðskiptaskuldir** – Opnar lánardrottnafærslur (reikninga sem hafa ekki verið greiddir).
- **Fjárhagsfærslur** – Færslur þar sem tilgreint er að bókun muni eiga sér stað í framtíðinni.
- **Færslur í fjárhagsáætlunarskrá** – Færslur í fjárhagsáætlunarskrá sem eru valdar fyrir sjóðstreymisspár.
- **Eftirspurnarspár** – Línur í birgðaspálíkani sem eru valdar fyrir sjóðstreymisspár.
- **Birgðaspá** – Línur í birgðaspálíkani sem eru valdar fyrir sjóðstreymisspár.

Jafnvel þótt engin bein samþætting sé milli verkefnastjórnunar og bókhalds eru nokkrar leiðir til að hafa verkfærslur með í sjóðstreymisspánni. Bókaðir verkreikningar eru hafðir með í spánni sem hluti af opnum viðskiptamannafærslum. Sölu- og innkaupapantanir sem koma úr verkefnum eru innifaldar í spánum sem opnar pantanir eftir að þær eru færðar inn í kerfið. Einnig er hægt að flytja verkspár í fjárhagsáætlunarlíkan. Þetta fjárhagsáætlunarlíkan er síðan tekið með í sjóðstreymisspá sem hluti af færslum í fjárhagsáætlun.

## <a name="configuration"></a>Grunnstilling

Til að skilgreina sjóðstreymisspá skal nota síðuna **Uppsetning sjóðstreymisspár**. Á þessari síðu eru tilgreindir greiðslugetulyklar til að fylgjast með sjálfgefinni spávirkni fyrir hvert svæði.

### <a name="general-ledger"></a>Fjárhagur

Það verður fyrst að skilgreina greiðslugetulykla til að fylgjast með sjóðstreymisspá. Yfirleitt eru þessar greiðslugetulyklar aðallyklar sem tengjast bankareikningum sem taka á móti og greiða út reiðufé. Á síðunni **Uppsetning sjóðstreymisspár** á flipanum **Fjárhagur** skal velja aðallykla sem eiga að vera með í spám. Ef bankareikningur hefur verið tengdur aðallykli á síðunni **Bankareikningur** birtist hann á svæðinu **Bankareikningur**.

Hægt er að setja upp háða sjóðsstreymisspá fyrir aðallykil sem inniheldur færslur sem tengjast færslum beint í öðrum aðallykli. Hver lína sem er bætt við í hlutanum **Í háðum lyklum** stofnar upphæð fyrir sjóðstreymisspá í háðum aðallykli. Þessi upphæð er prósentuhlutfall sjóðstreymisupphæðar af aðallyklinum sem var valinn.

Fyrst þarf að setja svæðið **Aðallykill** á fyrsta aðallykilinn þar sem færslur myndast væntanlega í upphafi. Stilltu svæðið **Háður aðallykill** á lykilinn sem verður fyrir áhrifum af upphaflegu færslunni gagnvart fyrsta aðallyklinum. Stilltu viðeigandi gildi á öðrum svæðum í línunni. Hægt er að breyta gildinu í svæðinu **Prósenta** svo það endurspegli áhrif fyrsta aðallykils á háðan aðallykil. Ef um er að ræða sölu- eða innkaupaspá skal velja gildi fyrir **Greiðsluskilmála** sem er dæmigert fyrir flesta viðskiptavini eða lánardrottna. Stilltu svæðið **Bókunargerð** á væntanlega bókunargerð sem tengist sjóðstreymisspánni.

### <a name="accounts-payable"></a>Viðskiptaskuldir

Hægt að reikna út innkaupaspána með því að nota uppsetningarvalmöguleikana á flipanum **Viðskiptaskuldir** á síðunni **Sjóðstreymisspá**. Áður en hægt er að skilgreina sjóðsstreymisspá fyrir viðskiptaskuldir þarf að skilgreina greiðsluskilmála greiðslu, lánardrottnaflokka og bókunarreglur lánardrottna.

Í hlutanum **Sjálfgildi innkaupaspár** er hægt að velja sjálfgefna innkaupavirkni fyrir sjóðstreymisspá. Þrjú svæði ákvarða tímasetningu áhrifa á lausafé: **Tími milli afhendingardagsetningar og reikningsdagsetningar**, **Greiðsluskilmálar** og **Tími milli gjalddaga reiknings og greiðsludagsetningar**. Spáin notar ekki sjálfgefna stillingu fyrir svæðið **Greiðsluskilmálar** nema ekkert gildi sé tilgreint í færslunni. Notaðu greiðsluskilmála til að lýsa dæmigerðasta dagafjölda fyrir hvern hluta ferlisins.

Svæðið **Greiðslugetulyklar fyrir greiðslur** tilgreinir þann greiðslugetulykil sem oftast er notaður fyrir greiðslur. Notaðu svæðið **Prósentuhlutfall af upphæð sem úthluta á sjóðsstreymisspá** til að tilgreina hvort eigi að nota prósentu af upphæð við spá. Hafðu þennan reit auðan ef nota á fullar færsluupphæðir við spá.

Hægt er að hnekkja sjálfgefinni tímastillingu fyrir **Tíma milli gjalddaga reiknings og dagsetningar greiðslu** fyrir tiltekna lánardrottnahópa. Spáin notar sjálfgildið úr hlutanum **Sjálfgildi innkaupaspár** nema annað gildi sé tilgreint fyrir lánardrottnahópinn sem tengist þeim lánardrottni sem er í færslunni. Til að hnekkja sjálfgefna gildinu skal velja lánardrottnahóp og stilla svo nýja gildið fyrir svæðið **Innkaupatími**.

Hægt er að hnekkja sjálfgefnum stillingum fyrir svæðið **Greiðslugetulykill** fyrir tilteknar bókunarreglur lánardrottins. Spáin notar sjálfgildið úr hlutanum **Sjálfgildi innkaupaspár** nema annar greiðslugetulykill sé tilgreindur fyrir bókunarregluna sem tengist þeim lánardrottni sem er í færslunni. Til að hnekkja sjálfgefna gildinu skal velja bókunarreglu og tilgreina svo greiðslugetulykilinn sem áætlað er að verði fyrir áhrifum.

### <a name="accounts-receivable"></a>Viðskiptakröfur

Hægt er að reikna út söluspána með því að nota uppsetningarvalmöguleikana á flipanum **Viðskiptakröfur** á síðunni **Sjóðstreymisspá**. Áður en hægt er að skilgreina sjóðsstreymisspá fyrir viðskiptakröfur þarf að skilgreina greiðsluskilmála greiðslu, viðskiptavinaflokka og bókunarreglur viðskiptavina.

Í hlutanum **Sjálfgildi söluspár** er hægt að velja sjálfgefna söluvirkni fyrir sjóðstreymisspá. Þrjú svæði ákvarða tímasetningu áhrifa á lausafé: **Tími milli sendingardagsetningar og reikningsdagsetningar**, **Greiðsluskilmálar** og **Tími milli gjalddaga reiknings og greiðsludagsetningar**. Spáin notar ekki sjálfgefna stillingu fyrir svæðið **Greiðsluskilmálar** nema ekkert gildi sé tilgreint í færslunni. Notaðu greiðsluskilmála til að lýsa dæmigerðasta dagafjölda fyrir hvern hluta ferlisins. 

Svæðið **Greiðslugetulyklar fyrir greiðslur** tilgreinir þann greiðslugetulykil sem oftast er notaður fyrir greiðslur. Notaðu svæðið **Prósentuhlutfall af upphæð sem úthluta á sjóðsstreymisspá** til að tilgreina hvort eigi að nota prósentu af upphæð við spá. Hafðu þennan reit auðan ef nota á fullar færsluupphæðir við spá.

Hægt er að hnekkja sjálfgefinni tímastillingu fyrir **Tíma milli gjalddaga reiknings og dagsetningar greiðslu** fyrir tiltekna viðskiptavinaflokka. Spáin notar sjálfgildið úr hlutanum **Sjálfgildi söluspár** nema annað gildi sé tilgreint fyrir lánardrottnahópinn sem tengist þeim viðskiptavini sem er í færslunni. Til að hnekkja sjálfgefna gildinu skal velja viðskiptavinaflokk og stilla svo nýja gildið fyrir svæðið **Sölutími**.

Hægt er að hnekkja sjálfgefnum stillingum fyrir svæðið **Greiðslugetulykill** fyrir tilteknar bókunarreglur viðskiptavinar. Spáin notar sjálfgildið úr hlutanum **Sjálfgildi sölupár** nema annar greiðslugetulykill sé tilgreindur fyrir bókunarregluna sem tengist þeim viðskiptavini sem er í færslunni. Til að hnekkja sjálfgefna gildinu skal velja bókunarreglu og tilgreina svo greiðslugetulykilinn sem áætlað er að verði fyrir áhrifum.

### <a name="budgeting"></a>Fjárhagsáætlanir

Hægt er að taka með fjárhagsáætlanir sem stofnaðar eru úr áætlunarlíkönum í sjóðstreymisspám. Á flipanum **Fjárhagsáætlun** á síðunni **Uppsetning sjóðstreymisspár** skal velja áætlunarlíkön til að taka með í spá. Það er sjálfgefið að nýjar færslur í fjárhagsáætlunarskrá séu hafðar með í spám eftir að áætlunarlíkanið hefur verið virkjað fyrir sjóðstreymisspá. Hægt er að skrifa yfir meðtalningu í sjóðstreymisspá í einstökum færslum í fjárhagsáætlunarskrá.

### <a name="inventory-management"></a>Birgðir

Hægt er að taka spár fyrir birgðaframboð og eftirspurn með í sjóðstreymisspám. Á flipanum **Birgðastjórnun** á síðunni **Uppsetning sjóðstreymisspár** skal velja spálíkön til að taka með í sjóðstreymisspá. Hægt er að skrifa yfir meðtalningu í sjóðstreymisspá í einstökum línum í spá um framboð og eftirspurn.

### <a name="calculation"></a>Útreikningur

Áður en hægt er að skoða greiningar sjóðstreymisspár verður að keyra útreikningsferli fyrir sjóðstreymi. Útreikningsferlið framreiknar framtíðaráhrif á lausafé vegna færslna sem hafa verið skráðar.

Reiknaðu sjóðstreymisspá með því að nota síðuna **Reikna sjóðstreymisspár**. Hægt er að reikna annaðhvort fulla sjóðsstreymisspá eða stigvaxandi sjóðsstreymisspá. 

- Til að hreinsa allar færslur í sjóðstreymisspá og endurreikna skal stilla svæðið **Reikniaðferð sjóðstreymisspár** á **Heildarupphæð**. Mælt er með því að nota þessa nálgun ef sjóðstreymisspár hafa ekki verið uppfærðar í lengri tíma. 
- Til að uppfæra fyrirliggjandi upplýsingar sjóðstreymisspár fyrir nýjar færslur skal stilla svæðið **Reikniaðferð sjóðstreymisspár** á **Nýtt**. Síðan sýnir þá dagsetningu þegar útreikningur á sjóðstreymi var síðast keyrður.

Einnig er hægt að nota runuvinnslu í sjóðsstreymisspá. Til að tryggja að spágreiningar séu reglulega uppfærðar skal setja upp endurtekna runuvinnslu á útreikningum fyrir sjóðstreymisspár.

### <a name="reporting"></a>Skýrslur

Eftir að sjóðsstreymisspá er reiknuð þarf að endurnýja tengdar einingarupplýsingar fyrir greiningarskýrslur. Á síðunni **Einingaverslun** skal velja mælinguna **uppsafnaðar LedgerCovLiquidityMeasurement** og smella svo á **Endurnýja**.

Tvö vinnusvæði innihalda gögn fyrir sjóðstreymisspár. Eitt vinnusvæði hefur að geyma gögn fyrir öll fyrirtæki og hitt aðeins gögn fyrir núverandi fyrirtæki.

Aðgangi að vinnusvæði fyrir öll fyrirtæki er stjórnað gegnum í aðgangsheimildina **Skoða vinnusvæði fyrir sjóðstreymi allra fyrirtækja**. Vinnusvæðið **Yfirlit yfir reiðufé – öll fyrirtæki** er sjálfgefið fyrir eftirtalin hlutverk:

- Forstjóri
- Fjármálastjóri
- Fjármálastjóri

Aðgangi að vinnusvæði fyrir núverandi fyrirtæki er stjórnað gegnum í aðgangsheimildina **Skoða vinnusvæði fyrir sjóðstreymi núverandi fyrirtækis**. Vinnusvæðið **Yfirlit yfir reiðufé – núverandi fyrirtæki** er sjálfgefið fyrir eftirtalin hlutverk:

- Bókhaldari
- Bókhaldsstjóri
- Yfirmaður bókhalds
- Viðskiptaskuldastjóri
- Viðskiptakröfustjóri

Vinnusvæðið **Yfirlit yfir reiðufé – öll fyrirtæki** sýnir greiningar fyrir sjóðstreymisspár í gjaldmiðli kerfisins. Gjaldmiðill kerfis og gengisgerð sem notuð er í greiningunni er skilgreind á síðunni **Kerfisfæribreytur**. Þetta vinnusvæði sýnir yfirlit yfir sjóðstreymisspár og stöðu bankareikninga allra fyrirtækja. Línurit yfir sjóðsinnstreymi og útstreymi gefur yfirlit yfir framtíðarhreyfingar lausafjár og stöðu í gjaldmiðli kerfisins ásamt ítarlegum upplýsingum um spáðar færslur. Einnig má sjá spáðar gengisstöður.

Vinnusvæðið **Yfirlit yfir reiðufé – núverandi fyrirtæki** sýnir greiningar fyrir sjóðstreymisspá í skilgreindum bókhaldsgjaldmiðli fyrirtækisins. Bókhaldsgjaldmiðillinn sem er notaður fyrir greiningu er skilgreindur á síðunni **Fjárhagur**. Þetta vinnusvæði sýnir yfirlit yfir sjóðstreymisspár og stöðu bankareikninga núverandi fyrirtækis. Línurit yfir sjóðsinnstreymi og útstreymi gefur yfirlit yfir framtíðarhreyfingar lausafjár og stöðu í bókhaldsgjaldmiðli ásamt ítarlegum upplýsingum um spáðar færslur. Einnig má sjá spáðar gengisstöður.

Sjá flipann Tilvísunarstig Power BI fyrir frekari upplýsingar um framleiðslustig.

Þar að auki er hægt að skoða gögn sjóðstreymisspár fyrir tiltekna lykla, pantanir og vörur á eftirfarandi síðum:

- **Prófjöfnuður**: Veldu **Sjóðstreymisspár** til að skoða framtíðarsjóðstreymi fyrir þann aðallykil sem valinn er.
- **Allar sölupantanir**: Á flipanum **Reikningur** skal velja **Sjóðstreymisspár** til að skoða spáð áhrif valdrar sölupöntunar á lausafé.
- **Allar innkaupapantanir**: Á flipanum **Reikningur** skal velja **Sjóðstreymisspár** til að skoða spáð áhrif valdrar innkaupapöntunar á lausafé.
- **Birgðaspá**: Velja **Sjóðstreymisspár** til að skoða komandi útstreymi lausafjár sem tengist birgðaspá valdrar vöru.
- **Eftirspurnarspá**: Velja **Sjóðstreymisspár** til að skoða komandi útstreymi lausafjár sem tengist eftirspurnarspá valdrar vöru.

