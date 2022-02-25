---
title: Sjóðstreymisspár
description: Þetta efnisatriði gefur yfirlit yfir ferli sjóðstreymisspár. Það útskýrir einnig hvernig sjóðstreymisspá er samþætt við aðrar einingar í kerfinu.
author: panolte
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5a46946ff2c3569dab0ce8b53b3cddcf18318cbf
ms.sourcegitcommit: 465c84eb5cdc211692e2ae09b45d1400f9a315ee
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2022
ms.locfileid: "8314721"
---
# <a name="cash-flow-forecasting"></a>Sjóðstreymisspár

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Hægt er að nota verkfæri fyrir sjóðstreymisspár til að greina væntanlegt sjóðstreymi og gjaldeyrisþörf þannig að hægt sé að meta framtíðarþörf fyrirtækis fyrir lausafé. Til að gera spá um sjóðstreymi þarf fyrst að gera eftirfarandi:

- Greina og fá lista yfir alla greiðslugetulykla. Greiðslugetulyklar eru lausafjárreikningar fyrirtækis eða jafngildi þeirra.
- Skilgreina virkni spáa á færslum sem hafa áhrif á greiðslugetulykla fyrirtækisins.

Þegar þessu er lokið er hægt að reikna og greina sjóðstreymisspár og væntanlega gjaldeyrisþörf.

## <a name="cash-flow-forecasting-integration"></a>Samþætting á sjóðstreymisspám

Hægt er að samþætta sjóðstreymisspár við fjárhag, viðskiptaskuldir, viðskiptakröfur, fjárhagsáætlun og birgðastjórnun. Spáferlið notast við færsluupplýsingar sem eru skráðar í kerfið og útreikningarnir spá fyrir um væntanleg áhrif hverrar færslu á lausafé. Eftirfarandi færslur eru teknar með í reikninginn við útreikninga á sjóðstreymi:

- **Sölupantanir** – Sölupantanir sem ekki hafa verið reikningsfærðar og verða að efnislegri eða fjárhagslegri sölu.
- **Ókeypis textareikningar** – Reikningar með frjálsum texta sem ekki hafa verið bókaðir enn og leiða til fjársölu. 
- **Innkaupapantanir** – Innkaupapantanir sem ekki hafa verið reikningsfærðar og verða að efnislegum eða fjárhagslegum innkaupum.
- **Viðskiptakröfur** – Opnar viðskiptamannafærslur (reikninga sem hafa ekki verið greiddir).
- **Viðskiptaskuldir** – Opnar lánardrottnafærslur (reikninga sem hafa ekki verið greiddir).
- **Fjárhagsfærslur** – Færslur þar sem tilgreint er að bókun muni eiga sér stað í framtíðinni.
- **Færslur í fjárhagsáætlunarskrá** – Færslur í fjárhagsáætlunarskrá sem eru valdar fyrir sjóðstreymisspár.
- **Eftirspurnarspár** – Línur í birgðaspálíkani sem eru valdar fyrir sjóðstreymisspár.
- **Birgðaspá** – Línur í birgðaspálíkani sem eru valdar fyrir sjóðstreymisspár.
- **Ytri gagnagjafi** - Ytri gögn sem eru færð inn eða flutt inn í sjóðstreymisspár með því að nota töflureiknisniðmát.
- **Verkspár** - Verkefnastjórnun og bókhaldsspár með spárlíkani.
- **Greiðslur sjóðstreymi söluskattsyfirvalda** – Áætluð greiðsluupphæð söluskattsyfirvalda og tímasetning sem leiða til fjárgreiðslna. Virkjaðu eiginleikann Greiðslur sjóðstreymis skattyfirvalda.

## <a name="configuration"></a>Skilgreining

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

Hægt er að taka með fjárhagsáætlanir sem stofnaðar eru úr áætlunarlíkönum í sjóðstreymisspám. Á síðunni **Uppsetning sjóðstreymisspár** á flipanum **Fjárhagsáætlun** skal velja áætlunarlíkön til að taka með í spá. Það er sjálfgefið að nýjar færslur í fjárhagsáætlunarskrá séu hafðar með í spám eftir að áætlunarlíkanið hefur verið virkjað fyrir sjóðstreymisspá.

Hægt er að hafa færslur fjárhagsáætlunarskráar í sjóðstreymisspánni á einstaklingsgrunni í gegnum sérstillingu. Þegar þú bætir dálknum „Telja með í sjóðstreymisspám“ við síðuna **Færsla í fjárhagsáætlunarskrá** mun kerfið skrifa yfir stillingarnar á síðunni **Uppsetning sjóðsstreymisspár** til að hafa með staka færslu í fjárhagsáætlunarskrá í spánni.


### <a name="inventory-management"></a>Birgðir

Hægt er að taka spár fyrir birgðaframboð og eftirspurn með í sjóðstreymisspám. Á flipanum **Birgðastjórnun** á síðunni **Uppsetning sjóðstreymisspár** skal velja spálíkön til að taka með í sjóðstreymisspá. Hægt er að skrifa yfir meðtalningu í sjóðstreymisspá í einstökum línum í spá um framboð og eftirspurn.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Setja upp vídd fyrir sjóðsstreymisspá
Nýr flipi á **Uppsetning sjóðstreymisspár**  síða gerir þér kleift að stjórna hvaða fjárhagsvíddir verða notaðar til að sía í **Sjóðstreymisspá**  vinnurými. Þessi flipi mun aðeins birtast þegar eiginleiki sjóðstreymisspár er virkur.

Á flipanum **Víddir** skal velja víddir af listanum sem á að nota fyrir síun og nota örvalyklana til að fara þá í dálkinn til hægri. Aðeins er hægt að velja tvær víddir til að sía spárgögn sjóðstreymisspár. 

### <a name="setting-up-external-source"></a>Setja upp ytri uppsprettu
Ytri gögn er hægt að færa inn eða flytja inn í sjóðstreymisspár þegar Finance Insights hefur verið stillt. Áður en ytri gögn eru færð inn eða flutt inn verður að setja upp ytri heimildir. Á **Ytri heimild** flipa, setja upp ytri sjóðstreymisflokka. Flokkur getur verið **Sendandi** eða **Komandi**. **Lausafjárstaða** ætti að vera valin sem færslugerð. Í **Stillingar lögaðila** grid, velja lögaðila og tilheyrandi aðalreikninga sem ytra sjóðstreymisflokkar eiga við.

Fyrir frekari upplýsingar, sjá [Ytri gögn í sjóðstreymisspám](../../finance/finance-insights/external-data-in-cash-flow.md). 

### <a name="project-management-and-accounting"></a>Verkefnastjórnun og bókhald

Í útgáfu 10.0.17 gerir nýr eiginleiki samþættingu verkefnastjórnunar og bókhalds- og sjóðstreymisspáa mögulega. Á vinnusvæðinu **Eiginleikastjórnun** skal kveikja á eiginleikanum **Sjóðstreymisspá verks** til að taka með spákostnað og tekjur í sjóðstreymisspá. Á flipanum **Verkefnastjórnun og bókhald** á síðunni **Uppsetning sjóðsstreymisspár** skal velja þær verkgerðir og færslugerðir sem á að taka með í sjóðstreymisspá. Veljið svo verkspárlíkan. Undirlíkan fyrir minnkunargerð virkar best. Greiðslugetulyklarnir sem voru færðir inn í uppsetningu viðskiptakrafna eru notaðir sem sjálfgefinn greiðslugetulyklar. Þess vegna þarf ekki að færa inn sjálfgefna greiðslugetulykilal þegar sjóðstreymisspá er sett upp. Einnig er hægt að nota áætlunarlíkan en aðeins er hægt að velja eina gerð á síðunni **Uppsetning sjóðsstreymisspár** fyrir verkefnastjórnun og bókhald. Spárííkan veitir mestan sveigjanleika við notkun verkefnastjórnunar og bókhald eða Project Operations.

Þegar kveikt er á eiginleika sjóðstreymis fyrir verk er hægt að skoða sjóðstreymisspá fyrir hvert verk á síðunni **Öll verk**. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Spá**, skal velja **Sjóðstreymisspá**. Á **Yfirlit yfir reiðufé** vinnusvæðum (sjá hlutann [Skýrslugerð](#reporting) síðar í þessu efnisatriði), sýnir spáfærslugerð innflæði (tekjur spáfærslu) og útflæði (kostnað spáfærslu). Aðeins er hægt að taka upphæðirnar með ef reiturinn **Verkefnastig** í **Yfirlit yfir reiðufé** vinnusvæði er stilltur á **Í vinnslu**.

Verkfærslur eru enn innifaldar í sjóðstreymisspá á marga vegu, óháð því hvort kveikt sé á eiginleikanum **Sjóðstreymisspá verks** eða ekki. Bókaðir verkreikningar eru hafðir með í spánni sem hluti af opnum viðskiptamannafærslum. Sölu- og innkaupapantanir sem koma úr verkefnum eru innifaldar í spánum sem opnar pantanir eftir að þær eru færðar inn í kerfið. Einnig er hægt að flytja verkspár í fjárhagsáætlunarlíkan. Þetta fjárhagsáætlunarlíkan er síðan tekið með í sjóðstreymisspá sem hluti af færslum í fjárhagsáætlun. Ef kveikt er á eiginleikanum **Sjóðstreymisspá verks** skaltu ekki fleyjta verkspár í fjárhagsáætlunarlíkan, vegna þess að aðgerðin mun valda því að verkspárnar séu tvítaldar.

### <a name="sales-tax-authority-payments"></a>Greiðslur söluskattyfirvalda 

Eiginleikinn Greiðslur á sjóðstreymi söluskattsyfirvalda spáir fyrir um sjóðstreymisáhrif söluskattsgreiðslna. Það notar ógreiddar söluskattsfærslur, skattuppgjörstímabil og greiðslutímabil skatttímabilsins til að spá fyrir um dagsetningu og upphæð sjóðstreymisgreiðslna. 

### <a name="calculation"></a>Útreikningur

Áður en hægt er að skoða greiningar sjóðstreymisspár verður að keyra útreikningsferli fyrir sjóðstreymi. Útreikningsferlið framreiknar framtíðaráhrif á lausafé vegna færslna sem hafa verið skráðar.

Reiknaðu sjóðstreymisspá með því að nota síðuna **Reikna sjóðstreymisspár**. Hægt er að reikna annaðhvort fulla sjóðsstreymisspá eða stigvaxandi sjóðsstreymisspá. 

- Til að hreinsa allar færslur í sjóðstreymisspá og endurreikna skal stilla svæðið **Reikniaðferð sjóðstreymisspár** á **Heildarupphæð**. Mælt er með því að nota þessa nálgun ef sjóðstreymisspár hafa ekki verið uppfærðar í lengri tíma. 
- Til að uppfæra fyrirliggjandi upplýsingar sjóðstreymisspár fyrir nýjar færslur skal stilla svæðið **Reikniaðferð sjóðstreymisspár** á **Nýtt**. Síðan sýnir þá dagsetningu þegar útreikningur á sjóðstreymi var síðast keyrður.

Einnig er hægt að nota runuvinnslu í sjóðsstreymisspá. Til að tryggja að greiningarspárnar séu uppfærðar reglulega skal setja upp endurtekna runuvinnslu fyrir útreikning á sjóðsstreymisspá.

Í útgáfu 10.0.13, var gefin út viðbót við reikningsferlið sem notar ramma sjálfvirkniferlis til að áætla reikningsverk sjóðstreymis. Þetta er gert virkt með því að nota eiginleikann **Sjálfvirkni sjóðstreymisspár** á vinnusvæðinu **Eiginleikastjórnun**. Þegar þetta er virkt skal velja tengilinn **Sjálfvirkni sjóðstreymisspár** til að birta nýju sjálfvirknisíðuna þar sem hægt er að áætla útreikningsferli sjóðstreymis. Til að stofna nýja áætlun sjóðstreymisspár skal velja **Stofna nýjan sjálfvirkan ferli** og velja **Sjálfvirkni sjóðstreymisspár** í fellivalmyndinni **Gerð áætlunar**. Setja verður áætlun fyrir hvert fyrirtæki þar sem verið er að uppfæra gögn sjóðsstreymisspár fyrir.  Þessi síða sýnir einnig hvaða sjálfvirku verk sjóðsstreymisspár eru í bið og hvenær síðasta verkinu var lokið.  

> [!NOTE] 
> Ef fyrirliggjandi runuvinnslur eru þegar tímasettar fyrir sjóðsstreymisspár birtast villuboð og ekki verður hægt að virkja þennan eiginleika. Hreinsa þarf fyrirliggjandi runuvinnslur áður en hægt er að virkja þennan eiginleika. 

Frekari upplýsingar er að finna í [Sjálfvirkni ferlis](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

### <a name="reporting"></a>Skýrslugerð

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

Sjá [Sjóðsstreymi Power BI](Cash-Overview-Power-BI-content.md) fyrir frekari upplýsingar um greiningarspár fyrir sjóðsstreymi.

Þar að auki er hægt að skoða gögn sjóðstreymisspár fyrir tiltekna lykla, pantanir og vörur á eftirfarandi síðum:

- **Prófjöfnuður**: Veldu **Sjóðstreymisspár** til að skoða framtíðarsjóðstreymi fyrir þann aðallykil sem valinn er.
- **Allar sölupantanir**: Á flipanum **Reikningur** skal velja **Sjóðstreymisspár** til að skoða spáð áhrif valdrar sölupöntunar á lausafé.
- **Allar innkaupapantanir**: Á flipanum **Reikningur** skal velja **Sjóðstreymisspár** til að skoða spáð áhrif valdrar innkaupapöntunar á lausafé.
- **Birgðaspá**: Velja **Sjóðstreymisspár** til að skoða komandi útstreymi lausafjár sem tengist birgðaspá valdrar vöru.
- **Eftirspurnarspá**: Velja **Sjóðstreymisspár** til að skoða komandi útstreymi lausafjár sem tengist eftirspurnarspá valdrar vöru.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
