---
title: "Skýrsluhönnunarviðmót"
description: "Þessi grein útskýrir hvernig á að fara gegnum Report Designer og hvernig á að nota mismunandi valkostir til að uppfylla sérstakar kröfur fyrirtækisins."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 50 - 10
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 58c56aca6f339a5ec13703605334dd45b208ab2c
ms.lasthandoff: 03/29/2017


---

# <a name="report-designer-interface"></a>Skýrsluhönnunarviðmót

Þessi grein útskýrir hvernig á að fara gegnum Report Designer og hvernig á að nota mismunandi valkostir til að uppfylla sérstakar kröfur fyrirtækisins. 

<a name="report-designer-menu-commands"></a>Skýrsluhönnunarvalmyndarskipanir
-----------------------------

Eftirfarandi töflur lýsa skipanir fyrir valmyndinni og valkosti sem hægt er að nota þegar hannaðar eru fjárhagsskýrslur. Sumar skipanir og valkostir valmynda eru einungis í boði við tilteknar kringumstæður. Til dæmis skipanir fyrir promoting og demoting skýrslugerðareiningar eru aðeins tiltækar þegar verið er að breyta skilgreiningu skipurits.

### <a name="file-menu"></a>Valmynd Skrá

Valmyndin **Skrá** er í boði fyrir alla notendur og inniheldur eftirfarandi skipanir.

| Skipun                           | Lýsing                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nýjar                               | Stofna nýja skýrsluskilgreiningu, línuskilgreiningu, skilgreiningu dálks, skilgreiningu skipurits, skýrsluhópsskilgreiningu, eða möppu. Eftirfarandi valkostir eru tiltækir, eftir hlutverki notanda. |
| Opna                              | Opna fyrirliggjandi línuskilgreiningu, dálkskilgreiningu, skipuritsskilgreiningu eða skýrsluskilgreiningu.                                                                                             |
| Loka                             | Loka gildandi einingahóp.                                                                                                                                                                |
| Loka öllu                         | Loka öllum einingahópum.                                                                                                                                                                       |
| Vista                              | Vista fyrirliggjandi línuskilgreiningu, dálkskilgreiningu, skipuritsskilgreiningu eða skýrsluskilgreiningu.                                                                                             |
| Vista sem                           | Vista núverandi línuskilgreiningu, dálkskilgreiningu, skipuritsskilgreiningu eða skýrsluskilgreiningu undir nýju heiti.                                                                            |
| Eiginleikar                        | Opna skal **Eiginleika** svarglugga þar sem hægt er að breyta heiti og lýsingu á skýrslu.                                                                                                   |
| Mynda                          | Mynda núverandi skýrslu. Þessi skipun er í boði í skýrsluskilgreiningu.                                                                                                                 |
| Skoða skýrslu                       | Opna nýjustu útgáfu skýrslunnar mynduð í Dynamics 365 fyrir Aðgerðir. Þessi skipun er tiltæk úr skilgreiningu skýrslu ef mynduð hefur verið a.m.k. ein skýrsla.                                 |
| Nýlegar skýrsluskilgreiningar         | Sýna lista yfir skýrslur sem hafa nýlega verið stofnaðar eða breytt. Þá er hægt að velja skýrslu á listanum.                                                                                    |
| Nýlegar línuskilgreiningar            | Sýna lista yfir línuskilgreiningar sem hafa nýlega verið stofnaðar eða breytt. Þá er hægt að velja línuskilgreiningu á listanum.                                                                    |
| Nýlegar dálkskilgreiningar         | Sýna lista yfir dálkskilgreiningar sem hafa nýlega verið stofnaðar eða breytt. Þá er hægt að velja dálkskilgreiningu á listanum.                                                              |
| Nýlegar skilgreiningar skipurits | Sýna lista yfir skipuritsskilgreiningar sem hafa nýlega verið stofnaðar eða breytt. Þá er hægt að velja skilgreiningu skipurits á listanum.                                              |
| Hætta                              | Hætta í Skýrsluhönnun.                                                                                                                                                                            |

### <a name="edit-menu"></a>Valmyndin Breyta

**Breyta** valmyndin er tiltæk fyrir notendur sem hafa hlutverkið **Hönnuður** eða **Kerfisstjóri**. Þessi valmynd hefur meðal annars eftirfarandi skipanir.

| Skipun                                | Lýsing                                                                                                                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Afturkalla                                   | Afturkalla síðustu aðgerð.                                                                                                                                                                                              |
| Endurgera                                   | Hætta við að Afturkalla síðustu aðgerð.                                                                                                                                                                                      |
| Klippa                                    | Eyða völdum texta og afrita hann á klippiborðið.                                                                                                                                                            |
| Afrita                                   | Afrita valdan texta og setja á klippiborðið.                                                                                                                                                                           |
| Líma                                  | Setja inn nýjasta klippta eða afritaða texta af klippiborðinu.                                                                                                                                                    |
| Hreinsa                                  | Eyða innihaldi valins einingahópareits.                                                                                                                                                           |
| Finna                                   | Opna skal **Finna og skipta út** svarglugga þar sem hægt er að leita að texta í rúðunni skoða.                                                                                                                              |
| Skipta út                                | Opna skal **Finna og skipta út** svarglugga þar sem hægt er að leita að og skipta út texta í rúðunni skoða.                                                                                                                  |
| Setja inn línur úr víddum            | Opna skal **Setja inn línur úr víddum** svarglugga þar sem hægt er að velja víddargildi sem á að taka með í línuskilgreiningu. Þessi skipun er í boði í línuskilgreiningu.                                  |
| Endurnúmera línur                          | Endurnúmera allar tölulega línu kóða. Þessi skipun er í boði í línuskilgreiningu.                                                                                                                                   |
| Línutenglar                              | Opna **Línu Tengla** svarglugga þar sem hægt er að tilgreina uppruna fyrir gagnatengla í línuskilgreiningum og skilgreiningum skipurits. Þessi skipun er í boði í línuskilgreiningu.                            |
| Sléttunarleiðréttingar                    | Opna skal **Sléttunarleiðréttingar** svarglugga þar sem hægt er að tilgreina færibreytur fyrir sléttun. Þessi skipun er í boði í línuskilgreiningu.                                                                  |
| Vinna með víddasamstæður                  | Opna skal **Víddasamstæðu** svarglugga, þar sem hægt er að stofna og breyta víddasamstæðum. Þessi skipun er tiltæk úr línuskilgreiningu eða skilgreiningum skipurits.                                              |
| Setja inn línu                             | Setja auða línu inn í línuskilgreiningu eða auða fyrirsagnalínu í skilgreiningu dálks. Þessi skipun er tiltæk úr línuskilgreiningu eða skilgreiningum skipurits.                                               |
| Eyða línu                             | Eyða valinni línu úr línuskilgreiningu eða valinni fyrirsagnalínu úr skilgreiningu dálks. Þessi skipun er tiltæk úr línuskilgreiningu eða skilgreiningum skipurits.                                       |
| Setja inn dálk                          | Setja auðan dálk inn í dálkskilgreininguna. Þessi skipun er í boði í dálkskilgreiningu.                                                                                                             |
| Eyða dálki                          | Eyða völdum dálki úr skilgreiningu dálks. Þessi skipun er í boði í dálkskilgreiningu.                                                                                                         |
| Setja inn einingar skipurits úr víddum | Opna skal **Setja inn einingar skipurits úr víddum** svarglugga þar sem hægt er að velja víddargildi sem á að taka með í skipuritsskilgreiningu. Þessi skipun er í boði í skipuritsskilgreiningu. |
| Flytja inn víddasamstæðustigveldi         | Opna skal **Víddasamstæðustigveldi** svarglugga þar sem hægt er að flytja inn víddasamstæðustigveldi úr fjárhagsgögnum. Þessi skipun er tiltæk úr skýrslugerð tré skilgreiningu á er við... kerfið \financial-dimensions\dimension-based.  |
| Setja inn einingu skipurits                  | Setja inn auða línu í skipuritsskilgreiningu. Þessi skipun er í boði í skipuritsskilgreiningu.                                                                                                |
| Eyða einingu skipurits                  | Eyða valdri skýrslugerðareiningarlínu úr skipuritsskilgreiningu. Þessi skipun er í boði í skipuritsskilgreiningu.                                                                             |

### <a name="view-menu"></a>Valmyndin skoða

**Skoða** valmyndin er tiltæk fyrir alla notendur og inniheldur eftirfarandi skipanir.

| Skipun         | Lýsing                                                            |
|-----------------|------------------------------------------------------------------------|
| Skoðunarrúða | Sýnið eða felið yfirlitssvæðið.                                      |
| Verkfæraslár        | Veljið verkfæraslár sem eru sýnilegar.                                  |
| Stöðustika      | Sýnið eða felið stöðuupplýsingarnar í glugganum **Skýrsluhönnun**. |
| Upphafssíða    | Opnið síðuna **Velkomin(n)**.                                             |

### <a name="format-menu"></a>Valmyndin Snið

**Snið** valmyndin er tiltæk fyrir notendur sem hafa hlutverk sem**Hönnuður** eða **Kerfisstjóri**. Þessi valmynd hefur meðal annars eftirfarandi skipanir.

| Skipun               | Lýsing                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stílar og snið | Opna skal **Stílar og Snið** svarglugga, þar sem hægt er að stofna og breyta stíl fyrir texta í línuskilgreiningum og dálkaskilgreiningum. Þessi skipun er tiltæk úr línuskilgreiningu eða skipuritsskilgreiningu. |
| Dálkbreidd          | Opna skal **Dálkabreidd** svarglugga þar sem hægt er að stilla breiddina í völdum dálki. Þessi skipun er tiltæk úr línuskilgreiningu eða skipuritsskilgreiningu.                      |
| Fela                  | Fela valinn dálk. Þessi skipun er tiltæk úr línuskilgreiningu eða skipuritsskilgreiningu.                                                                                        |
| Sýna                | Gera falda dálka milli valinna dálka sýnilega. Þessi skipun er tiltæk í línuskilgreiningu, dálkskilgreiningu eða skipuritsskilgreiningu.                                                      |

### <a name="company-menu"></a>Valmyndin Fyrirtæki

Valmyndin **Fyrirtæki ** er tiltæk fyrir notendur sem hafa hlutverk sem **Hönnuður** eða **Kerfisstjóri**. Þessi valmynd hefur meðal annars eftirfarandi skipanir.

| Skipun               | Lýsing                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Fyrirtæki             | Opna skal **Fyrirtæki** svarglugga, þar sem hægt er að stofna og breyta fyrirtækjum.                                          |
| Einingarhópar | Opna skal **Einingarhópar** svarglugga, þar sem hægt að stofna, breyta, flytja inn og út einingarhópa. |

### <a name="go-menu"></a>Valmyndin Áfram

Valmyndin **Áfram** er í boði fyrir alla notendur og inniheldur eftirfarandi skipanir. **Ábending:** Þessar skipanir hafa engin sýnileg áhrif nema yfirlitssvæðið sé sýnilegt.

| Skipanir                   | Lýsing                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Skýrsluskilgreiningar         | Sýna skýrsluskilgreiningar á yfirlitssvæðinu.                                    |
| Línuskilgreiningar            | Sýna línuskilgreiningar á yfirlitssvæðinu.                                       |
| Dálkskilgreiningar         | Sýna dálkskilgreiningar á yfirlitssvæðinu.                                    |
| Skilgreiningar skipurits | Sýna skilgreiningar skipurits á yfirlitssvæðinu.                            |
| Öryggi                   | Sýna upplýsingar um öryggi fyrir notendur, flokka og fyrirtæki á yfirlitssvæðinu. |

### <a name="tools-menu"></a>Valmyndin Verkfæri

Valmyndin**Verkfæri** er tiltæk fyrir alla notendur en sumar skipanir eru aðeins tiltækar að takmörkuðu leyti. Þessi valmynd hefur meðal annars eftirfarandi skipanir.

| Skipun                       | Lýsing                                                                                                                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verja                       | Nota aðgangsorð á núgildandi einingu. Þessi skipun er tiltæk fyrir notendur sem hafa hlutverk sem **Hönnuður** eða **Kerfisstjóri**.                                                                           |
| Biðraðarstaða skýrslu           | Opna skal **Biðraðarstaða skýrslu** svarglugga þar sem hægt er að sjá allar nýlega myndaðar skýrslur og upplýsingar fyrir hverja skýrslu.                                                                                    |
| Upprunakerfisupplýsingar     | Sýna stillingar fyrir Microsoft Dynamics ERP kerfið. Þessi skipun er tiltæk fyrir notendur sem hafa hlutverk sem **Hönnuður** eða **Kerfisstjóri**.                                                                 |
| Útskráð atriði             | Sýna línuskilgreiningar, dálkskilgreiningar, skilgreiningar skipurits og skýrsluskilgreiningar sem nú eru opin. Þessi skipun er tiltæk fyrir notendur sem hafa hlutverk sem **Hönnuður** eða **Kerfisstjóri**. |
| Uppfæra fjárhagsgögn í skyndiminni | Uppfæra gögn í dálknum fjárhagsvíddir.                                                                                                                                                               |
| Valréttarsamningar                       | Opna skal **Valkostir** svarglugga þar sem hægt er að breyta kjörstillingum notanda fyrir Skýrsluhönnun.                                                                                                                       |

### <a name="window-menu"></a>Valmyndin Gluggi

Valmyndin **Gluggi** er í boði fyrir alla notendur og inniheldur eftirfarandi skipanir.

| Skipun              | Lýsing                                                                                                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Raða lárétt    | Sýna alla opna glugga hlið við hlið.                                                                                                                                                     |
| Raða lóðrétt      | Sýna alla opna glugga í lóðréttri röð.                                                                                                                                               |
| Stallað              | Lagraða öllum opnum gluggum þannig að titilstikan fyrir hvern glugga sé sjáanleg.                                                                                                                      |
| Festa lárétt    | Frysta valda línu þannig að línan heldur áfram að vera sýnileg í glugganum þó þú flettir. Þessi skipun er tiltæk fyrir notendur sem hafa hlutverk sem **Hönnuður** eða **Kerfisstjóri**.       |
| Festa lóðrétt      | Frysta valinn dálk þannig að dálkurinn heldur áfram að vera sýnilegur í glugganum þó þú flettir. Þessi skipun er tiltæk fyrir notendur sem hafa hlutverk sem **Hönnuður** eða **Kerfisstjóri**. |
| Listi yfir opna glugga | Sýna lista yfir glugga sem eru opnir. Veljið glugga til að færa hann fremst.                                                                                                               |

### <a name="help-menu"></a>Valmyndin hjálp

**Hjálp** valmyndin er tiltæk fyrir alla notendur og inniheldur eftirfarandi skipanir.

| Skipun | lýsing                                                  |
|---------|--------------------------------------------------------------|
| Hjálp    | Opna Dynamics 365 fyrir Aðgerðir wiki hjálparsíðu fyrir fjárhagsskýrslugerð. |
|         |                                                              |

## <a name="report-designer-toolbar-buttons"></a>Skýrsluhönnunarverkfærahnappar
Eftirfarandi töflur lýsa hnöppum á verkfæraslá sem hægt er að nota þegar skýrslur eru hannaðar. Sumir hnappar á tækjastiku er einungis tiltækir við tilteknar kringumstæður. Til dæmis eru hnappar fyrir promoting og demoting skýrslueiningar aðeins tiltækir þegar verið er að breyta skilgreiningum skipurits.

### <a name="standard-toolbar"></a>Stöðluð tækjastika

Stöðluð tækjastika veitir þægilegan aðgang að skráar- og breytingaskipunum. Þessi tækjastika inniheldur eftirfarandi hnappa.

| Hnappur                                                                                                                                                                                   | Lýsing                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![New button](./media/rowc130389.png)](./media/rowc130389.png)                              | Stofna nýja (tóma) skýrsluskilgreiningu, línuskilgreiningu, dálkskilgreiningu eða skipuritsskilgreiningu.                                                                               |
| [![Opna hnappur](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Opna fyrirliggjandi línuskilgreiningu, dálkskilgreiningu, skipuritsskilgreiningu eða skýrsluskilgreiningu.                                                                                   |
| [![Vista hnappur](./media/savec130389.png)](./media/savec130389.png)                           | Vista fyrirliggjandi línuskilgreiningu, dálkskilgreiningu, skipuritsskilgreiningu eða skýrsluskilgreiningu.                                                                                   |
| [![Afrita hnappur](./media/copyc130389.png)](./media/copyc130389.png)                           | Afrita valdan texta og setja á klippiborðið.                                                                                                                                               |
| [![Klippa hnappur](./media/cutc130389.png)](./media/cutc130389.png)                              | Eyða völdum texta og afrita hann á klippiborðið.                                                                                                                                |
| [![Líma hnappur](./media/pastec130389.png)](./media/pastec130389.png)                        | Setja inn texta af klippiborðinu.                                                                                                                                                    |
| [![Afturkalla hnappur](./media/undoc130389.png)](./media/undoc130389.png)                           | Afturkalla síðustu aðgerð.                                                                                                                                                                  |
| [![Endurtaka hnappur](./media/redoc130389.png)](./media/redoc130389.png)                           | Hætta við að Afturkalla síðustu aðgerð.                                                                                                                                                          |
| [![Finna hnappur](./media/findc130389.png)](./media/findc130389.png)                           | Opna skal **Finna og Skipta út** svarglugga þar sem hægt er að leita að og skipta út texta í virkum glugga.                                                                                  |
| [![Setja inn línu hnappur](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Setja auða línu inn í línuskilgreiningu eða auða fyrirsagnalínu í skilgreiningu dálks. Þessi hnappur er tiltækur úr línuskilgreiningu eða dálkskilgreiningu.                    |
| [![Færa inn dálkur hnappur](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Setja auðan dálk inn í dálkskilgreininguna. Þessi hnappur er tiltækur í dálkskilgreiningu.                                                                                  |
| [![Læsa hnappur](./media/lockc130389.png)](./media/lockc130389.png)                           | Nota aðgangsorð á núgildandi einingu. Þessi hnappur er tiltækur fyrir notendur sem hafa hlutverkið **Hönnuður** eða **Kerfisstjóri**.                                                 |
| [![Tengja hnappinn línu](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Opna **Línu Tengla** svarglugga þar sem hægt er að tilgreina uppruna fyrir gagnatengla í línuskilgreiningum og skilgreiningum skipurits. Þessi hnappur er tiltækur í línuskilgreiningu. |
| [![Skýrsluþjónsgreining hnappur](./media/promotec130389.png)](./media/promotec130389.png)                  | Hækka einingu í skilgreiningu skipurits. Þegar þú velur undireiningu og smellir síðan á **Hækka**, er undireiningin flutt á sama stig og yfireining hennar.                |
| [![Demote hnappur](./media/demotec130389.png)](./media/demotec130389.png)                     | Lækka einingu í skilgreiningu skipurits. Þegar eining er valin og síðan smellt á **Lækka**, verður einingin undireining þeirrar einingar sem kemur á undan henni.                               |
| [![Útvíkka hnappur](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Stækka allar einingar í skipuritsskilgreiningunni á stigi valinnar einingar.                                                                                                   |
| [![Fella hnappur](./media/collapsec130389.png)](./media/collapsec130389.png)               | Fella saman skipuritið.                                                                                                                                                           |
| [![Hjálp fyrir hnapp](./media/helpc130389.png)](./media/helpc130389.png)                           | Opnið Hjálp.                                                                                                                                                                             |

### <a name="formatting-toolbar"></a>Sniðstika

Sniðstikan veitir auðveldan aðgang að sniðskipunum. Þessi tækjastika inniheldur eftirfarandi hnappa.

| Hnappur                                                                                                                                                                                                   | Lýsing                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Hnappurinn leturgerð stíl](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Nota valinn leturstíl á valinn texta.      |
| [![Hnappurinn leturgerð](./media/fonttype.png)](./media/fonttype.png)                                                 | Nota valda leturgerð á valinn texta.              |
| [![Stærð hnappinn leturgerð](./media/fontsize.png)](./media/fontsize.png)                                            | Nota valda leturstærð á valinn texta (í punktum). |
| [![Feitletrað hnappur](./media/boldc130389.png)](./media/boldc130389.png)                                           | Feitletra valinn texta.                             |
| [![Hnappurinn Skáletur](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Skáletra valinn texta.                           |
| [![Strika undir hnappur](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Undirstrika valinn texta.                             |
| [![Minnka inndrátt hnappur](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Minnka inndrátt valins texta.                |
| [![Auka inndrátt hnappur](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Auka inndrátt valins texta.                |
| [![Hnappurinn bakgrunnur lit](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Breyta bakgrunnslit valda hólfsins.        |
| [![Litur hnappinn leturgerð](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Breyta litnum á valda textanum.                   |

### <a name="report-designer-toolbar"></a>Tækjastikan skýrsluhönnun

Tækjastikan Skýrsluhönnun veitir auðveldan aðgang að skipunum til að fara um í skýrsluhönnun. Þessi tækjastika inniheldur eftirfarandi hnappa.

| Hnappur                                                                                                                                                                                          | Lýsing                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Hnappurinn skilgreiningu skýrslu](./media/reportc130389.png)](./media/reportc130389.png)                 | Sýna skýrsluskilgreiningar sem koma fram á valmyndinni **Gluggi**.                                                                                                            |
| [![Hnappurinn skilgreining línu](./media/rowc130389.png)](./media/rowc130389.png)                          | Sýna línuskilgreiningu sem tengist virku skýrsluskilgreiningunni.                                                                                                    |
| [![Hnappurinn skilgreining dálks](./media/columnc130389.png)](./media/columnc130389.png)                 | Sýna dálkskilgreiningu sem tengist virku skýrsluskilgreiningunni.                                                                                                 |
| [![Skilgreining hnappinn skýrslugerð tré](./media/treec130389.png)](./media/treec130389.png)             | Sýna skipuritsskilgreiningu sem tengist virku skýrsluskilgreiningunni.                                                                                         |
| [![Hnappurinn Viewer skýrslu](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Opnar Report Viewer og sýnir nýjustu útgáfu skýrslunnar sem hefur verið mynduð. Þessi skipun er tiltæk úr skilgreiningu skýrslu ef verið er að mynda a.m.k. eina skýrslu. |
| [![Mynda skýrslu hnappur](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Mynda skýrslu út frá virku skýrsluskilgreiningunni. Þessi hnappur er tiltækur í skýrsluskilgreiningu.                                                                      |



<a name="see-also"></a>Sjá einnig
--------

[Fjárhagsskýrslur fyrir Microsoft Dynamics ERP](financial-reporting-intro.md)

[Generate a financial report](\financials\general-ledger\generate-financial-report.md)


