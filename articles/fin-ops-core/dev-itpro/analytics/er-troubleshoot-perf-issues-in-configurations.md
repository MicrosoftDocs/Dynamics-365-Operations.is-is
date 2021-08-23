---
title: Úrræðaleita vandamál sem tengjast afköstum í skilgreiningum rafrænnar skýrslugerðar
description: Þetta efnisatriði útskýrir hvernig á að finna og laga vandamál sem tengjast afköstum í skilgreiningum rafrænnar skýrslugerðar.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b5f5308f171b6cd4224debec897dbde133e6d8424673aabfab51e6b83b9014e2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744387"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>Úrræðaleita vandamál sem tengjast afköstum í skilgreiningum rafrænnar skýrslugerðar

Þetta efnisatriði útskýrir hvernig á að finna og leysa vandamál sem tengjast afköstum í [skilgreiningum](general-electronic-reporting.md#Configuration) [rafrænnar skýrslugerðar](general-electronic-reporting.md).

Yfirleitt felur rannsókn á afköstum í sér nokkur skref.

1. [Safna](#collecting-data) gögnum.
2. Greinið söfnuð gögn.
3. Byggt á niðurstöðum greiningarinnar skal nota skilgreiningar rafrænnar skýrslugerðar til að [gera breytingar](#making-changes) eða taka ákvörðun um að safna meiri gögnum.

## <a name="troubleshooting"></a>Úrræðaleit

### <a name="analyze-execution-time"></a>Greina keyrslutíma

Keyrslutími getur verið háður óvæntum þáttum á borð við önnur verk sem keyra í sama umhverfinu og skyndiminni sem notar gögn þegar kallað er á það í fyrsta skipti. Þess vegna ætti að endurtaka framkvæmdina og mælinguna nokkrum sinnum.

Stundum koma upp afkastavandamál sem tengjast ekki skilgreiningu rafræns skýrslugerðarsniðs sem er notað í skýrslugerð. Þess í stað stafa þau af X++ kóðanum sem er notaður til að opna skilgreiningu rafræns skýrslugerðarsniðs.

1. Í annaðhvort [Aðgerðamiðstöðinni](#infolog-time) eða [tilvikakladdanum](#event-log-time) skal skoða keyrslutíma skýrslunnar.
2. Berið saman keyrslutíma skýrslunnar við heildartíma keyrslunnar í aðstæðunum.
3. Ef keyrslutími skýrslunnar er mun styttri en heildartími keyrslunnar skal skoða gagnamagnið sem skýrslan vinnur úr:

    - Ef skýrslan vinnur úr litlu gagnamagni gæti vandamálið tengst hleðslutíma skilgreiningarinnar.
    - Ef skýrslan vinnur úr miklu gagnamagni gæti vandamálið tengst forvinnslu X++. Notið [Rakningarþáttara](#analyze-trace-parser-trace) til að greina vandamálið.

    Sjáið næstu hluta fyrir annars konar vandamál.

4. Keyrið mörg próf sem fela í sér mismunandi gagnamagn til að fá úr því skorið hvort keyrslutíminn fari eftir gagnamagninu.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Greina rakningar rakningarþáttara

Undirbúið lítið sýnishorn eða safnið saman nokkrum rakningum á handahófskenndum tímapunktum skýrslumyndunar.

Gerið síðan hefðbundna alhliða greiningu í [Rakningarþáttara](#trace-parser) og svarið eftirfarandi spurningum:

- Hverjar eru helstu aðferðirnar hvað varðar tímanotkun?
- Hvaða hluta af heildartímanum nota þessar aðferðir?

Svarið sömu spurningunum fyrir fyrirspurnir.

Ef þú sérð að aðferðir hafa forskeytið „ER“ skaltu fara í næsta hluta.

Ef þú sérð að aðferðir eða fyrirspurnir eiga uppruna sinn í forritspakkanum skaltu íhuga almennar fínstillingar (til dæmis búa til atriðaskrá).

Greinið fjölda kalla. Ef talan er umtalsvert hærri en búist var við ætti að íhuga að vista samsvarandi hnúta skilgreiningarinnar í skyndiminni.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Greina gagnagrunnsköll

Undirbúið dæmi sem inniheldur lítið magn af gögnum þannig að hægt sé að safna [Rakningu rafrænnar skýrslugerðar](#electronic-reporting-traces).

Opnið síðan rakninguna í hönnuði líkanavörpunar rafrænnar skýrslugerðar og kíkið neðst á síðuna. Svarið eftirfarandi spurningum:

- Eru einhverjar tvítekningar á fyrirspurn? Ef svo er skaltu íhuga eina af eftirfarandi leiðréttingum:

    - [Notaðu vistun í skyndiminni](#use-caching) ef þú telur að mörg köll séu inni í einni yfirskrá.
    - [Notaðu færibreytustilltan reiknaðan reit sem vistaður er í skyndiminni](#cached-parameterized) ef þú telur að það séu köll í sömu færsluna inni í mismunandi færslum.
    - [Notaðu **JOIN** gagnagjafa](#use-join-datasource) ef nauðsyn reynist að lesa umtalsverðan fjölda af færslum úr gagnagrunni.

- Samræmist fjöldi fyrirspurna og sóttra færslna heildarfjölda gagna? Ef skjal hefur t.d. 10 línur, sýnir tölfræðin að skýrslan dragi út 10 línur eða 1000 línur? Ef talsverður fjöldi færslna er sóttur skal íhuga eina af eftirfarandi lagfæringum:

    - [Notið **FILTER** aðgerðina í stað **WHERE** aðgerðarinnar](#filter) til að vinna úr gögnum hjá SQL Server.
    - Notið vistun í skyndiminni til að forðast að sækja sömu gögnin.
    - [Notið söfnuð gögn](#collected-data) til að forðast að sækja sömu gögnin fyrir samantekt.

### <a name="analyze-perfview-traces"></a>Greina PerfView-rakningar

[PerfView](#perfview) er verkfæri fyrir reynda þróunaraðila. Ítarlegri upplýsingar um eftirfarandi skref er að finna í [Grunnatriði um tíma veggjaklukku](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Safnið saman rakningu með því að nota tíma þráðar.
2. Hafið aðeins með stafla sem nota **runUnattended** til að sía aðeins þráðinn sem er með skilgreiningarkeyrslu. (Bætið **runUnattended** við **IncPats** innsláttarreitinn.)
3. Fellið saman örgjörva, netkerfi og útilokaðan tíma.
4. Hlaðið inn [forstillingum rafrænnar skýrslugerðar fyrir PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).
5. Veljið **ER** \> **Önnur forstilling**.
6. Skoðið nöfnin:

    - Líklega sjáið þið verkvangskóðann sem notar mestan tímann.
    - Hægt er að tvípikka (eða tvísmella) og fara upp í gegnum **hringjendur**.

        Ef klasar finnast með forskeytinu „ERExpression“ og þeir eru aðgerðir sem tengjast formúlum er hægt að giska á heiti aðgerðarinnar út frá klasaheitinu og hægt er að kíkja á geymslu rafrænnar skýrslugerðar til að skoða eigindirnar.

### <a name="fixes"></a>Lagfæringar

- Ef kemur í ljós að mestur örgjörvatíminn fer í fyrirspurnir skal reyna að draga úr fjölda fyrirspurna:

    - [Farið yfir rakningu rafrænnar skýrslugerðar](#analyze-database-calls) fyrir tvíteknar fyrirspurnir.
    - Skoðið hversu margar færslur eru sóttar og metið hversu mikið af gögnum eigi fræðilega að sækja.

- Ef kemur í ljós að meirihluti örgjörvatíma fer í aðgerðir sem eru notaðar skal reyna að finna staðinn í skilgreiningunni sem notar flest tilföngin.
- Ef kemur í ljós að mestur örgjörvatími fer í aðgerðir gagnasöfnunar skal íhuga að skipta þeim út fyrir *SQL-flokka eftir* á síðu líkanavörpunar.

### <a name="collecting-data"></a><a name="collecting-data"></a>Safna gögnum

Til eru nokkrar leiðir til að safna tiltækum gögnum eftir umhverfinu þínu:

- Sækja heildarkeyrslutíma:

    - Úr aðgerðamiðstöðinni
    - Frá viðburðaferli

- Setjið saman keyrsluna:

    - Með því að nota verkfæri rafrænnar skýrslugerðar
    - Með því að nota rakningarþáttara
    - Með því að nota PerfView

#### <a name="collecting-data-in-a-production-environment"></a>Gagnasöfnun í vinnsluumhverfi

Stundum er eingöngu hægt að endurskapa vandamál í vinnsluumhverfi. Hægt er að safna gögnum á eftirfarandi hátt:

- Með því að nota rakningar [Rakningarþáttara](../perf-test/trace-trace-tutorial.md)
- Með því að nota rakningar [rafrænnar skýrslugerðarkeyrslu](trace-execution-er-troubleshoot-perf.md)
- Með því að nota heildartíma keyrslu

#### <a name="collecting-data-in-a-development-environment"></a>Gagnasöfnun í þróunarumhverfi

Auk þeirra verkfæra sem hægt er að nota í vinnsluuumhverfi eru til ýmis verkfæri sem hægt er að nota í þróunarumhverfi:

- Tilvikakladdi (Microsoft-Dynamics-ElectronicReporting). Þessi kladdi getur gefið þér heildartíma keyrslu.
- Algeng .NET-verkfæri á borð við PerfView.

Þróunarumhverfi veitir þér aukinn sveigjanleika til að gera tilraunir. Til dæmis er hægt að slökkva á skýrsluhlutum til að sjá hvaða áhrif það hefur á keyrslutíma.

### <a name="tools"></a><a name="tools"></a>Verkfæri

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Keyrslutími í aðgerðamiðstöðinni

Rafræn skýrslugerð getur sýnt keyrslutíma skilgreiningarinnar í aðgerðamiðstöðinni. Þessi valkostur virkar aðeins fyrir tiltekinn notanda og tiltekið fyrirtæki og aðeins fyrir gagnvirkar lotur. Til að gera þennan eiginleika aðgengilegan skal fylgja eftirfarandi skrefum.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Í svarglugganum **Færibreytur notanda** skal stilla valkostinn **Sýna tíma skráarmyndunar** á **Já**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Keyrslutími í tilvikakladdanum

1. Opnið Windows Event Viewer.
2. Undir **Forrits- og þjónustukladda** skal opna **Microsoft-Dynamics-ElectronicReporting/Operational**.
3. Leitið að tilvikum **FormatMapingRun** þar sem **EventID=2** vegna þess að þessi tilvik innihalda upplýsingarnar um liðinn tíma.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Rakningar rakningarþáttara 

Þar sem rafræn skýrslugerð er innfelld í X++ er hægt að nota algeng X++ verkfæri til að greina afköst. Frekari upplýsingar er að finna í [Gera rakningar með því að nota rakningarþáttara](../perf-test/trace-trace-tutorial.md).

Nokkrar takmarkanir eru á þessari nálgun. Þar sem hluti rafrænnar skýrslugerðar er felldur inn í C# verða ekki allar upplýsingar aðgengilegar. Hins vegar er hægt að skoða upplýsingar um gagnanotkun. Auk þess geta langar skýrslukeyrslur farið fram úr geymslumörkum rakningar.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER spor

Rafræn skýrslugerð getur safnað sínum eigin rakningum og hún hefur myndrænar framsetningar og greiningarverkfæri fyrir þessar rakningar. Frekari upplýsingar er að finna í [Rekja framkvæmd á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Þar sem bæði X++ og rafræn skýrslugerð eru felld inn ofan á .NET-verkvanginn er hægt að nota algeng .NET-verkfæri. Til dæmis er hægt að nota ókeypis [PerfView](https://github.com/Microsoft/perfview) verkfæri.

Einnig er hægt að safna gögnum úr skipanalínunni. Til dæmis safnar eftirfarandi forskrift Windows PowerShell keyrslutímanum þar til keyrsla á einhverju sniði er stöðvuð í vélinni.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Nokkrar takmarkanir eru á þessari nálgun. Þú verður að hafa stjórnandaaðgang að vélinni. Að auki þarftu að vera reyndur þróunaraðili þar sem lærdómsferlið er krefjandi.

### <a name="making-changes"></a><a name="making-changes"></a>Að gera breytingar

#### <a name="use-caching"></a><a name="use-caching"></a>Nota vistun í skyndiminni

Þrátt fyrir að vistun í skyndiminni dregur úr tímanum sem þarf til að sækja gögn aftur, kostar það minni. Notið vistun í skyndiminni í tilvikum þar sem fjöldi sóttra gagna er ekki mjög mikill. Frekari upplýsingar og dæmi sem sýnir hvernig á að nota vistun í skyndiminni er að finna í [Bæta líkanavörpun á grundvelli upplýsinga úr framkvæmdarakningu](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Nota færibreytustilltan reiknaðan reit sem vistaður er í skyndiminni

Stundum þarf að fletta upp gildum ítrekað. Sem dæmi má nefna reikningsheiti og reikningsnúmer. Til að spara tíma er hægt að búa til reiknaðan reit með færibreytum á efsta stigi og bæta svo reitnum við skyndiminnið.

Mælt er með því að aðferðin sé aðeins notuð þegar stærð gagna í skyndiminni er lítil. Frekari upplýsingar eru í [Bættu frammistöðu rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum með reiknaða reiti með færibreytum](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>Nota JOIN-gagnagjafi

**JOIN** gagnagjafi gerir kleift að sækja margar tengdar færslur í einni fyrirspurn. Ekki þarf að nota sérstaka fyrirspurn til að sækja hverja tengda færslu. Ef t.d. 1000 línur eru til staðar og gögn um hverja línu út frá tengslum verða fyrirspurnirnar samtals 1001 (= 1000 + 1). Ef **JOIN** gagnagjafi er notaður þarf aðeins að nota eina fyrirspurn til að sækja sömu gögnin. Frekari upplýsingar eru í [Notaðu JOIN gagnaheimildir í ER-líkanavörpun til að fá gögn úr mörgum töflum forrita](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Nota FILTER-aðgerðina í staðinn fyrir WHERE-aðgerðina

**[FILTER](er-functions-list-filter.md)** aðgerðin keyrir skilyrði á SQL-þjóni, en **WHERE** aðgerðin sækir öll gögn úr listanum, eina færslu í einu, og notar skilyrðið fyrir hverja færslu fyrir sig. Til dæmis ef velja á eina færslu af 1000. Ef notað er **WHERE** verða allar 1000 færslurnar sóttar. Ef hins vegar **FILTER** er notað verður nákvæmlega ein færsla sótt. **FILTER** getur einnig notað atriðaskrá gagnagrunnsins.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Aðgerðir gagnasöfnunar eða gagnagjafi uppsafnaðra gagna notað

Ef skilgreiningin er með *flokka eftir* þátt sem tekur saman gögn sem skýrsla sótti mun þátturinn sækja öll gögnin aftur. Með því að nota aðgerðir gagnasöfnunar gerir þú rafrænni skýrslugerð kleift að safna saman gögnum þegar sótt er í fyrsta skipti. Frekari upplýsingar er að finna í [Skilgreina snið rafrænnar skýrslugerðar til að gera talningu og samlagningu](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Endurskrifa hluta skilgreiningarinnar í X++

Rafræn skýrslugerð styður aðferðir til að kalla á töflur og klasa, þ.m.t. viðbætur. Íhugið að endurskrifa hluta líkanavörpunarinnar í X++ til að auka afköstin.

Rafræn skýrslugerð getur notað gögn frá eftirfarandi upprunum:

- Klösum (**hlutar** og **klasa** gagnagjöfum)
- Töflum (**töflu** og **töflufærslna** gagnagjöfum)

[API rafrænnar skýrslugerðar](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) býður einnig upp á leið til að senda fyrirframreiknuð gögn úr köllunarkóðanum. Forritapakkinn inniheldur fjölmörg dæmi um þessa nálgun.
