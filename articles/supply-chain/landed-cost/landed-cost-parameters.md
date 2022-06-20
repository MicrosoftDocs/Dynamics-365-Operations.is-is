---
title: Uppsetning á færibreytum heildarkostnaðar
description: Þessi grein lýsir því hvernig á að setja upp almennar upplýsingar og stillingar sem eru notaðar í kostnaðareiningunni fyrir landað kostnað fyrir bókun, stöðuuppfærslur, númeraraðir og hegðun.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 99dbe17d4e83c2c75d52ca3fd22a1772d8045355
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871979"
---
# <a name="landed-cost-parameters-setup"></a>Uppsetning á færibreytum heildarkostnaðar

[!include [banner](../../includes/banner.md)]

Notuð er síðan **Færibreytusíða heildarkostnaðar** til að setja á upp almennar upplýsingar og skilgreiningar sem eru notaðar í einingunni **Heildarkostnaður** fyrir bókun, stöðuuppfærslur, númeraraðir og hegðun. Uppsetningu færibreytanna er deilt á milli lögaðila og stjórnandi getur breyt þeim.

## <a name="open-the-landed-cost-parameters-page"></a>Opna færibreytusíðu heildarkostnaðar

Til að vinna með færibreyturnar skal fara í **Heildarkostnaður \> Uppsetning \> Færibreytur heildarkostnaðar** og síðan stilla reitina eins og lýst er í eftirfarandi undirhlutum.

![Færibreytusíða heildarkostnaðar.](media/landed-cost-parameters.png "Færibreytusíða heildarkostnaðar")

## <a name="general-tab"></a>Almennt

### <a name="general-fasttab"></a>Flýtiflipinn Almennt

Eftirfarandi tafla lýsir reitunum sem eru tiltækir í flýtiflipanum **Almennt** í flipanum **Almennt** á síðunni **Færibreytusíða heildarkostnaðar**.

| Stilling | lýsing |
|---|---|
| Nota flutningstaxta | Flutningstaxti er stilltur fyrir skilgreint tímabil og er notaður til að áætla kostnað á vörum sem nota marga gjaldmiðla. Stillið þennan valkost á *Já* til að nota flutningstaxta. |
| Gerð gengis | Sjálfgefið safn gengis sem er notað fyrir útreikninga á mörgum gjaldmiðlum fyrir ferð og kostnað hennar. |
| Uppfæra magn innkaupapöntunar | Veljið hvað gerist ef notandi breytir magni á innkaupapöntunarlínu:<ul><li>**Samþykkja** – Ferðamagn er leiðrétt sjálfkrafa.</li><li>**Viðvörun** – Ef lína er tengd við ferð er viðvörun sýnd, en ferðamagnið er uppfært.</li><li>**Villa** – Ef lína er tengd við ferð birtast villuskilaboð og ekki er hægt að uppfæra innkaupapöntunina. Þess vegna verður pöntunarlínan fyrst að vera fjarlægð úr ferðinni.</li></ul> |
| Uppfæra sjálfkrafa fjölda kassa | Þegar þessi valkostur er stilltur á *Já* eru öllum kössum safnað saman og sýndir á stigi ferðar og gáms. Þegar hann er stilltur á *Nei* er fjöldi kassa upphaflega stilltur á 0 (núll) og er hægt að breyta handvirkt eftir þörfum. |

### <a name="costing-fasttab"></a>Flýtiflipinn Bókun

Eftirfarandi tafla lýsir reitunum sem eru tiltækir í flýtiflipanum **Kostnaðarútreikningur** í flipanum **Almennt** á síðunni **Færibreytur heildarkostnaðar**.

| Stilling | lýsing |
|---|---|
| Bókunarlýsing | Veljið leiðréttingu gildis í fjárhagnum:<ul><li>**Samtala** – heildartala er bókuð í fjárhaginn.</li><li>**Vöruflokkur** – Leiðréttingin er tilgreind eftir vöruflokki.</li><li>**Vörunúmer** – Leiðréttingin er tilgreind fyrir hverja vöru. Þetta gildi veitir ítarlegustu upplýsingarnar.</li></ul> |
| Leyfa núll kostnað | Stillið þennan valkost á *Nei* til að sýna villu ef notandi reynir að bóka kostnaðaráætlun fyrir reikning ferðar eða innkaupapöntun sem inniheldur ekki gildi fyrir væntanlegan kostnað ferðar. Villuboðin gefa til kynna að ekki er hægt að úthluta kostnað upp á 0 (núll) og bókun reiknings mun ekki takast. Í þessu tilviki getur notandinn uppfært matið handvirkt (eða endurskilgreint sjálfvirka kostnaðinn) og síðan annaðhvort tekið inn uppfært gildi eða eytt kostnaðinum ef hann á ekki við.<p>Stillið þennan valkost á *Já* til að kostnaður ferðir geti verið auður. Í þessu tilvikum verður verðinu 0 (núll) úthlutað samkvæmt kostnaðarsvæði. Þá er hægt að vinna aftur úr kostnaðarreikningi lánardrottins á móti kostnaðarverði núll þegar ferðin er móttekin.</p><p>Mælt er með því að skilgreina áætlun kostnaðarfærslunnar til að koma í veg fyrir að núll í kostnað birtist. Þótt þessi áætlun sé ekki hárrétt ætti hún samt sem áður að vera nákvæmari en að áætla núll í kostnað.</p> |
| Bókunardagsetning leiðréttingar | Þegar bókaður er kostnaðarreikningur fyrir ferð viðskiptaskulda er uppgjörstaflan (birgðaleiðréttingar) einnig uppfærð. Veljið dagsetninguna sem er stillt að sjálfgefnu á síðunni **Velja kostnað ferðar** í reikningabókinni:<ul><li>**Færsludagsetning** – Nota dagsetningu færslubókar (bókunardagsetning).</li><li>**Reikningsdagsetning innkaupapöntunar** – Notið fjárhagslega bókunardagsetningu birgðareikningsins (innkaupapöntunar).</li><li>**Valin dagsetning** – Notandinn getur tilgreint bókunardagsetningu. Þó að hægt sé að skilja dagsetninguna eftir auða, ef hún er enn auð þegar kostnaðarreikningur er bókaður, fær notandinn upp villu.</li></ul> |
| Nota fylgiskjal innkaupareiknings | Þegar þessi valkostur er stilltur á *Já* nota færslur uppsafnaðs kostnaðar sama fylgiskjalsnúmer og er notað fyrir innkaupareikninginn. Þegar hann er stilltur á *Nei* notar kerfið næsta tiltæka númer fyrir númeraröðina **Fylgiskjal uppsafnaðs kostnaðar** sem er sett upp í flipanum **Númeraraðir** á síðunni **Færibreytur heildarkostnaðar**.<p>Þessi valkostur hefur aðeins áhrif þegar valkosturinn **Bóka á gjaldalykil í fjárhag** er stilltur á *Já* í flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda**.</p> |
| Loka fyrir handvirka bókun á millireikning | Stillið þennan valkost á *Já* til að koma í veg fyrir að bókað sé á millireikninga þar sem færslan hefur ekki verið tengd við ferð með því að velja **Aðgerðir \> Velja kostnað ferðar** á aðgerðasvæði reikningabókar lánardrottins. Mælt er með að þessi valkostur sé stilltur á *Já* þannig að hægt sé að jafna ferðina og millireikninginn á réttan hátt. |
| Nota gjaldauppsöfnunarlykil kostnaðargerðar | Þegar þessi valkostur er stilltur á *Já* verður gjaldauppsöfnunarlykillinn sem er skilgreindur fyrir viðeigandi kostnaðargerðakóða á síðunni **Kostnaðargerðakóðar** notaður til að safna upp kostnaði sem útgjöldum.<p>Þessi valkostur hefur aðeins áhrif þegar valkosturinn **Bóka á gjaldalykil í fjárhag** er stilltur á *Já* í flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda**. |
| Bóka leiðréttingar sem frávik | Þegar þessi valkostur er stilltur á *Já* hnekkir það staðlaðri virkni og neyðir færslur birgðaleiðréttingar sem tengjast frávikum á milli áætlaðs kostnaðar og raunkostnaðar til að vera bókaðar á frávikslykil.<p>Þegar þessi valkostur er stilltur á *Nei* eru færslur birgðaleiðréttingar sem tengjast frávikum meðhöndlaðar samkvæmt skilgreiningu kostnaðarútreiknings og kostnaðargerðakóða. Fyrir staðalkostnað verða frávik samt bókuð á frávikslykilinn. Fyrir hlaupandi vegið meðaltal verða frávik bókuð annaðhvort á frávikalykilinn eða birgðirnar.</p><p>Þessi valkostur hefur aðeins áhrif þegar valkosturinn **Bóka á gjaldalykil í fjárhag** er stilltur á *Já* í flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda**.</p> |

### <a name="validation-fasttab"></a>Flýtiflipi staðfestingar

Eftirfarandi tafla lýsir reitunum sem eru tiltækir í flýtiflipanum **Staðfesting** í flipanum **Almennt** á síðunni **Færibreytur heildarkostnaðar**.

| Stilling | lýsing |
|---|---|
| Margir kostnaðarreikningar | Veljið hvað gerist ef unnið er úr fleiri en einum reikningi á móti ferð, fólíó eða gámi fyrir sama gjaldið.<ul><li>**Samþykkja** – Kerfið ætti að leyfa marga kostnaðarreikninga.</li><li>**Viðvörun** – Viðvörun er sýnd.</li><li>**Villa** - Villuboð birtast.</li></ul> |
| Margir lánardrottnar á hvert fólíó | Veljið hvað gerist ef fleiri en einni innkaupapöntun lánardrottins er bætt við fólíó.<ul><li>**Samþykkja** – Kerfið ætti að leyfa aðgerðina.</li><li>**Viðvörun** – Viðvörun birtist, en enn er hægt að framkvæma aðgerðina.</li><li>**Villa** – Billuboð eru sýnd og ekki er hægt að velja aðgerðina.</li></ul><p>Tollamiðlari eða staðbundin lög kunna krefjast sérstakra gilda fyrir þetta svæði.</p> |
| Vikmörk margra flutningsmáta | Veljið hvað gerist ef vörur úr innkaupapöntun, sem nota annan flutningsmáta en ferðin, er bætt við ferðina.<ul><li>**Samþykkja** – Kerfið ætti að leyfa aðgerðina.</li><li>**Viðvörun** – Viðvörun birtist, en enn er hægt að framkvæma aðgerðina.</li><li>**Villa** – Billuboð eru sýnd og ekki er hægt að velja aðgerðina.</li></ul> |
| Vikmörk margra vöruhúsa | Veljið hvað gerist ef ferð inniheldur nokkrar pöntunarlínur sem þarf að afhenda í mismunandi vöruhús. Þessar pöntunarlínur gætu verið dreifðar um eina innkaupapöntun eða margar.<ul><li>**Samþykkja** – Kerfið ætti að leyfa aðgerðina.</li><li>**Viðvörun** – Viðvörun er sýnd.</li><li>**Villa** - Villuboð birtast.</li></ul> |
| Rúmmál vantar | Veljið hvað gerist ef notandi bætir við vöru án magns við ferð.<ul><li>**Samþykkja** – Kerfið ætti að samþykkja vöruna.</li><li>**Viðvörun** – Viðvörun er sýnd.</li><li>**Villa** - Villuboð birtast.</li></ul><p>Ef rúmmál er notað til að reikna út og skipta kostnaði er mælt með því að velja annaðhvort *Viðvörun* eða *Villu*.</p> |
| Þjónustuaðili án ferðakostnaðar | Veljið hvað gerist ef notandi reynir að vinna úr reikningi fyrir þjónustuveitu sem hefur ekki verið tengd við ferð. <ul><li>**Samþykkja** – Kerfið ætti að leyfa aðgerðina.</li><li>**Viðvörun** – Viðvörun er sýnd.</li><li>**Villa** - Villuboð birtast.</li></ul><p>Mælt er með að velja *Viðvörun*.</p> |

### <a name="defaults-fasttab"></a>Flýtiflipi sjálfgilda

Eftirfarandi tafla lýsir reitunum sem eru tiltækir í flýtiflipanum **Sjálfgefið** í flipanum **Almennt** á síðunni **Færibreytur heildarkostnaðar**.

| Stilling | lýsing |
|---|---|
| Heiti færslubókar | Veljið sjálfgefnu færslubókina sem aðgerðin *Stofna komubók* á að nota. |
| Staða ferðar | Veljið stöðuna sem ferð verður að hafa áður en notendur geta sett upp leigðan flutningsgám í henni í kerfinu. Þessi aðgerð á sér yfirleitt stað þegar vörurnar eru í flutningi eða á höfninni. |
| Sniðmát ferðar | Veljið sjálfgefið sniðmát ferðar til að nota fyrir nýja leigða flutningsgáma. Yfirleitt er valið ferðasniðmát sem inniheldur leigukostnað. |
| Hreyfing | Ef yfir-/undirmagn fyrir afhendingu er innan skilgreindra vikmarka verður sjálfkrafa unnið úr hreyfingabók. Veljið sjálfgefna hreyfingabók til að nota. Reiturinn **Mótlykill** fyrir valið heiti færslubókar verður að hafa gildi. |
| Millifærsla | Þegar unnið er úr undirafhendingu verður of lítið móttekið magn flutt inn á vöruhús undirafhendingar. Veljið sjálfgefna flutningsbók til að nota. |
| Gera innkaupapantanir með engan flutning óvirkar | Slökkvið á aðgerð yfir-/undirafhendingar heildarkostnaðar fyrir innkaupapantanir sem ekki eru hengdar við ferð. |
| Gera innkaupapantanir með engar vörur í flutningi óvirkar | Slökkvið á aðgerð yfir-/undirafhendingar heildarkostnaðar fyrir innkaupapantanir sem nota ekki aðgerðina vörur í flutningi. |
| Vörur í flutningi yfir biðtíma innhreyfingar | Tilgreinið fjölda daga eftir fyrstu móttöku á flutningsgámi sem frekari yfirmóttökur er enn hægt að ljúka fyrir þann flutningsgám. |

## <a name="status-updates-tab"></a>Flipi stöðuuppfærslna

Kerfið notar stöðugildin til að gefa til kynna stöðu hverrar ferðar. Hægt er að nota sjálfkrafa stöðugildi ferða á ferðir í gegnum rakningu eða reglubundnar runuvinnslur ferðar. Að öðrum kosti er hægt að setja þau á handvirkt með því að opna ferðina og velja síðan stöðu í flokknum **Uppfærsla ferðar** í flipanum **Stjórna** á aðgerðasvæðinu. 

Hægt er að stofna eins mörg stöðugildi ferðar og þörf krefur. Hins vegar þarf að skilgreina fjórar þeirra sem notaðar eru í sérstökum tilgangi í flipanum **Stöðuuppfærslur** á síðunni **Færibreytur heildarkostnaðar**. Eftirfarandi tafla lýsir svæðum sem eru tiltæk þar.

| Stilling | lýsing |
|---|---|
| Kostnaðarútreikningur | Veljið ferðastöðuna sem gefur til kynna að ferð sé lokið. |
| Í flutningi | Veljið ferðastöðuna sem gefur til kynna að ferð sé í flutningi. |
| Tilbúið fyrir kostnaðarútreikning | Veljið ferðastöðuna sem gefur til kynna að ferð sé tilbúin fyrir kostnaðarútreikning. Þessi staða er notuð þegar búið er að vinna úr öllum innkaupareikningum birgða og kostnaðarreikningum ferðar þar sem reiturinn **Kredit á ferðakostnaði** er stilltur á *Lánardrottinn* fyrir ferðina. Ferðir þar sem ferli kostnaðarútreiknings tekst ekki fá stöðuna *Tilbúið fyrir kostnaðarútreikning*.|
| Kostað fyrirfram | Veljið ferðastöðuna sem gefur til kynna að ferð sé kostuð fyrirfram. Þessi staða er notuð þegar nýrri kostnaðarfærslu er bætt við ferð þegar búið er að kosta hana. Hægt er að bæta nýjum kostnaðarfærslum við fyrri kostaða ferð þegar annar farmreikningur eða óvænt biðdagaþóknun er móttekin. Þessi staða er sjálfkrafa notuð þegar nýjum kostnaði ferðar er bætt við kostaða ferð. |

## <a name="voyage-creator-tab"></a>Flipi ferðastofnanda

Eftirfarandi tafla lýsir hlutunum í flipanum **Stofnandi ferðar** á síðunni **Færibreytur heildarkostnaðar**.

| Kafli | lýsing |
|---|---|
| Leyfileg frávik | Reitirnir **Vikmörk rúmmáls** og **Vikmörk þyngdar** skilgreina efri mörk þegar vörur eru taldar með of mikið rúmmál og mikla þyngd. Þegar notandi bætir við vörum á síðunni **Ritill ferðar**, ef rúmmál eða þyngd fer umfram gildið er stillt hér, sýnir kerfið viðvörun. Gildi hvers reits er gefið upp sem prósenta af hámarksrúmmáli eða -þyngd sem er stillt fyrir viðeigandi gerð flutningagáms. Mælt er með því að gildið sé á bilinu 5 til 10 prósent af hámarksrúmmáli eða þyngd. |
| Uppsetning fyrir stofnun fólíós | Kerfið getur búið til mörg fólíó í stofnferli ferðar. Notið þennan hluta til að skilgreina hvenær stofna á nýtt fólíó. Fyrir hverja línu í þessum hluta kannar kerfið tilgreinda töflu og reit og stofnar fólíó fyrir hvert einkvæmt reitargildi. |

## <a name="cost-estimates-tab"></a>Flipi kostnaðarmats

Flipinn **Kostnaðarmat** á síðunni **Færibreytur heildarkostnaðar** gefur aðeins upp einn reit: **Sjálfgefin kostnaðarútgáfa**. Þessi reitur á aðeins við þegar aðferð kostnaðarútreiknings er *Staðlaður kostnaður*. Veljið sjálfgefna kostnaðarútgáfu sem á að nota fyrir reglubundna verkið *Uppfærsla á kostnaðarverði vöru*. Hugsanlega þarf að breyta þessari stillingu í hvert skipti sem nýtt fjárhagsár hefst.

## <a name="inventory-dimensions-tab"></a>Flipi birgðavídda

Notið flipann **Birgðavíddir** á síðunni **Færibreytur heildarkostnaðar** til að stýra því hvaða tiltækar birgðavíddir eigi að sýna að sjálfgefnu á hverri síðu heildarkostnaðar þar sem víddir eru notaðar.

Veljið vídd og stillið síðan valkostina **Línur ferðar**, **Vörur í flutningi** og/eða **Kostnaðarmat** á *Já* fyrir hverja síðu þar sem sýna á víddina að sjálfgefnu. Endurtakið þetta skref fyrir aðrar víddir eftir þörfum.

Stillingarnar á þessum flipa koma á fót sjálfgefnum víddunum fyrir hverja úthlutaða síðu í öllum lögaðilum. Hins vegar geta notendur sem eru að vinna í einni af úthlutuðu síðunum hnekkt sjálfgefnum víddum með því að velja **Birgðir \> Birta víddir** á aðgerðasvæðinu.

## <a name="number-sequences-tab"></a>Flipinn Númeraraðir

Flipinn **Númeraraðir** á síðunni **Færibreytur heildarkostnaðar** sýnir hverja gerð af tilvísunarnúmeraröð sem heildarkostnaður þarf, en sem er ekki deilt yfir alla lögaðila. Fyrir hverja tilvísun í listanum skal velja kóða númeraraðar.

> [!NOTE]
> Í skilgreiningu margra fyrirtækja verður að stofna mismunandi númeraraðir fyrir hvert fyrirtæki (lögaðilann).

## <a name="shared-number-sequences-tab"></a>Flipi fyrir samnýttar númeraraðir

Flipinn **Samnýttar númeraraðir** á síðunni **Færibreytur heildarkostnaðar** sýnir hverja gerð af tilvísunarnúmeraröð sem er samnýtt yfir lögaðila fyrir heildarkostnað. Eins og er er bara ein númeraröð í listanum. Þessi númeraröð er notuð fyrir ferðakennið.

Á síðunni **Allar ferðir** geta notendur skoðað ferðir allra lögaðila. Til að breyta og vinna úr ferð þurfa notendur hins vegar að vera í lögaðila valdrar færslu.

## <a name="feature-visibility-tab"></a>Flipi fyrir sýnileiki eiginleika

Heildarkostnaður bætir eiginleikum (reitum og aðgerðum) við nokkrar algengar síður í Microsoft Dynamics 365 Supply Chain Management. Þessar síður fela í sér síður sem tengjast aðalsniðmáti lánardrottins, útgefnum afurðum, innkaupapöntunum, flutningspöntunum og uppsetningu vöruhúss. Ef verið er að nota heildarkostnað verður að gera þessa eiginleika sýnilega allstaðar áður en hægt er að nota þá. Ef heildarkostnaður er ekki notaður er hægt að fela eiginleikanum svo þeir þvælist ekki fyrir.

Í flipanum **Sýnileiki eiginleika** á síðunni **Færibreytur heildarkostnaðar** skal stilla valkostinn **Virkja** á *Já* til að gera eiginleika heildarkostnaðar sýnilega þar sem þeir eru í boði. Stillið það á *Nei* til að fela eiginleikana á algengum síðum utan heildarkostnaðar. Hins vegar, jafnvel þegar valkosturinn er stilltur á *Nei*, mun sjálf einingin, þ.m.t. síðan **Færibreytur heildarkostnaðar**, vera áfram tiltæk notendum sem eru með réttar aðgangsheimildir.
