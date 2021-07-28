---
title: Kennsla í Regression Suite Automation Tool
description: Þetta efni sýnir hvernig á að nota Regression Suite Automation Tool (RSAT). Það lýsir ýmsum eiginleikum og gefur dæmi sem nota ítarlegar forskriftir.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: d932a0c10df72dbadcc65d7ef78eb8ad05645bd5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357519"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Kennsla í Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Notaðu verkfæri þín í internetvafranum til að sækja og vista þessa síðu á pdf-sniði.

Þetta kennsluefni fer í gegnum nokkra ítarlega eiginleika Regression Suite Automation Tool (RSAT), inniheldur sýniúthlutun og lýsir stefnu og lykilatriðum.

## <a name="notable-features-of-rsat-and-task-recorder"></a>Athyglisverðir eiginleikar RSAT og verkskráning

### <a name="validate-a-field-value"></a>Villuleita reitargildi

RSAT gerir þér kleift að setja staðfestingarskref í prófatilvikið þitt til að staðfesta vænt gildi. Upplýsingar um þennan eiginleika er að finna í greininni [Staðfesta væntanleg gildi](rsat-validate-expected.md).

Eftirfarandi dæmi sýnir hvernig hægt er að nota þennan eiginleika til að sannreyna hvort lagerbirgðir séu meiri en 0 (núll).

1. Í kynningargögnum í fyrirtækinu **USMF** skaltu stofna verkskráningu sem er með eftirfarandi skref:

    1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
    2. Nota flýtiafmörkun til að finna færslur Til dæmis sía gildið í reitnum **1000** fyrir reitinn **Vörunúmer**.
    3. Veldu **Lagerbirgðir**.
    4. Nota flýtiafmörkun til að finna færslur Til dæmis, sía á gildinu **1** fyrir reitinn **Vefsvæði**.
    5. Í listanum skal merkja valda línu.
    6. Sannprófaðu að gildi reitsins **Samtals magn til ráðstöfunar** sé **411,0000000000000000**.

2. Vistið verkskráningu sem **skráningu þróunaraðila** og hengið hana við prófunardæmið í Azure DevOps.
3. Bættu prófunardæminu við prófunaráætlunina og settu prófunardæmið í RSAT.
4. Opnið Excel-færibreytuskrána og farið í flipann **TestCaseSteps**.
5. Til að sannprófa hvort lagerbirgðir muni alltaf verða meiri en **0** skal fara í skrefið **Sannprófa samtals til ráðstöfunar** og breyta gildi þeirra úr **411** í **0**. Breytið gildinu í reitnum **Virknitákn** úr samasemmerki (**=**) í stærra en merki (**\>**).
6. Vistaðu og lokaðu Excel-færibreytskránni.
7. Veldu **Hlaða upp** til að vista breytingarnar sem þú gerðir í Excel-færibreytuskránni í Azure DevOps.

Nú, ef gildi reitsins **Samtals magn til ráðstöfunar** fyrir tilgreint atriði í birgðum er meira en 0 (núll), prófanir munu standast, óháð raunverulegu gildi lagerbirgða.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Vistaðar breytur og keðjupróf

Eitt af lykileiginleikunum í RSAT er keðja prófunardæma, það er að segja, geta prófunar til að gefa breytur til annarra prófana. Nánari upplýsingar er að finna í greininni [Afrita breytur í keðjuprófatilfelli](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Afleitt prófunardæmi

RSAT gerir þér kleift að nota sömu verkefnaskráningu með mörgum prófatilvikum, sem gerir verki kleift að keyra með mismunandi gagnaskipan. Sjá greinina [Afleidd prófunartilvik](rsat-derived-test-cases.md) fyrir meiri upplýsingar.

### <a name="validate-notifications-and-messages"></a>Staðfesta tilkynningar og skilaboð

Þennan eiginleika er hægt að nota til að staðfesta hvort aðgerð hafi átt sér stað. Til dæmis, þegar framleiðslupöntun er stofnuð, áætluð og síðan hafin sýnir forritið skilaboðin „Production - Start“ til að tilkynna þér að framleiðslupöntun hafi verið hafin.

![Framleiðsla – Ræsa tilkynningu.](./media/use_rsa_tool_05.png)

Þú getur valið þessi skilaboð í gegnum RSAT með því að slá inn skilaboðartexta á flipann **MessageValidation** í Excel-færibreytuskránni fyrir viðeigandi skráningu.

![Flipinn Sannprófun skilaboða.](./media/use_rsa_tool_06.png)

Þegar prófunardæmið hefur verið keyrt eru skilaboðin í Excel-færibreytuskránni borin saman við skilaboðin sem birtast. Ef skilaboðin stemma ekki mun prófunardæmið ekki takast.

> [!NOTE]
> Þú getur slegið inn fleiri en eina skilaboð á flipann **MessageValidation** í Excel-færibreytuskránni. Skilaboðin geta einnig verið villuboð eða viðvörunarboð í stað upplýsingaboða.

### <a name="snapshot"></a>Skyndimynd

Þessi eiginleiki tekur skjámyndir af þeim skrefum sem voru gerð meðan á verkskráningu stóð. Það er gagnlegt fyrir endurskoðun eða kembiforrit.

- Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Þegar þú keyrir prófunartilvikið mun RSAT búa til myndatökur (myndir) af skrefunum í spilunarmöppunni á prófatilvikunum í vinnumiðstöðinni. Ef verið er að nota eldri útgáfu af RSAT eru myndirnar vistaðar í **C:\\Notendur\\\<Username\>\\AppData\\Roaming\\regressionTool\\spilun**, aðskilin mappa er búin til fyrir hvert prófunartilvik sem er keyrt.

## <a name="assignment"></a>Verkefni

### <a name="scenario"></a>Aðstæður

1. Vöruhönnuður stofnar nýja útgefna vöru.
2. Framleiðslustjóri setur framleiðslufyrirmæli af stað til að koma birgðastigi í tvær einingar.
3. Framleiðsla byrjar og endar framleiðslupöntunina og staðfestir að magnið í lagerbirgðum sé tvær einingar.
4. Söluhópurinn fær pöntun um fjögur stykki af nýrri afurð. Þess vegna uppfærir söluhópurinn nettóþarfirnar í gegnum kviku áætlunina. Þar sem engin viðbótargeta er til staðar er sjálfgefin pöntunarregla stillt á „kaupa í stað þess að búa til“. Þess vegna er innkaupatillaga stofnuð.
5. Kaupandi bætir við lánardrottni, staðfestir áætlaða innkaupapöntun og staðfestir síðan innkaupapöntunina.
6. Þegar vörurnar sem voru keyptar koma í verslunina leitar verslunarrekandinn að viðkomandi innkaupapöntun og tekur á móti vörunum. Þar sem pöntuninni hefur nú verið lokið er hægt að taka vörurnar til og pakka á móti sölupöntuninni.
7. Fjármál birta innkaupareikning og sölureikning.

Eftirfarandi mynd sýnir flæðið fyrir þessar aðstæður.

![Flæði fyrir kynningaraðstæður.](./media/use_rsa_tool_14.png)

Eftirfarandi mynd sýnir stigveldi viðskiptaferla fyrir þessa atburðarás í LCS Viðskiptaferlavinnslu.

![Viðskiptaferli fyrir kynningaraðstæður.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Stjórnunarstefna – Lykilnám

### <a name="data"></a>Gögn

- Passaðu að þú hafir dæmigert gagnamagn (afrit af framleiðslu-/gullgrunnstillingargögnum auk yfirfærðra gagna).
- Þegar þú myndar ný gögn í gegnum verkskráningu skaltu stofna prófunarheiti sem munu ekki rekast á við fyrirliggjandi heiti (t.d. nota forskeyti eins og **RSATxxx**).
- Notaðu endurheimt Azure Point-In-Time til að endurkeyra prófanir í umhverfi sem ekki eru í 1. lagi.
- Þó að þú getir notað Excel-aðgerðirnar **RANDOM** og **NOW** til að mynda einkvæma samsetningu er framlagið tiltölulega hátt. Eftirfarandi er dæmi.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Verkskráning

- Skilgreindu aðstæður áður en þú hefur skráningu. Vel stýrt verk er með fyrirframskilgreindar prófunaraðstæður. Til að byggja upp prófunardæmi skaltu íhuga hversu fyrirsjáanleg niðurstaða þessara prófunaraðstæðna er.
- Skiptu skráningum ef þær eru gerðar með mismunandi hlutverkum eða ef það er biðtími eða utanaðkomandi viðburður á undan næsta skrefi.
- Forðastu að velja gildi í listum. Notaðu þess í stað textasnið, til dæmis **FIFO**, **AudioRM** og **SiteWH**. Þegar þú velur í lista er staðsetning gildis í listanum skráð, ekki gildið sjálft. Ef hlutum er bætt við listann getur staðsetning gildisins breyst. Þess vegna mun skráningin nota aðra færibreytu og afgangurinn af aðstæðunum gæti orðið fyrir áhrifum.
- Hugsaðu um hegðun fjölnotenda. Til dæmis skaltu ekki gera ráð fyrir að nýstofnuð sölupöntun þín verði alltaf sjálfkrafa valin. Notaðu þess í stað alltaf síuna til að finna réttu pöntunina.
- Notaðu virknina Afrita í verkskráningum til að vista heiti nýstofnaðrar afurðar þannig að hægt sé að nota það í keðjuðum prófunardæmum.
- Notaðu virknina Sannprófa í verkskráningunni til að stilla gátstaði sem staðfesta að skref hafi verið keyrð rétt.

### <a name="rsat"></a>RSAT

- Til að keyra prófið í öðru fyrirtæki geturðu breytt fyrirtækinu á flipanum **Almennt** í Excel-færibreytuskránni. Passaðu að stillingar og gögn séu tiltæk í nýja valda fyrirtækinu.
- Þú getur breytt prófnotanda á flipanum **Almennt** í Excel-færibreytuskránni. Tilgreindu netfang notandans mun keyra prófunardæmið. Þannig er hægt að keyra prófunardæmið með því að nota öryggisheimildir tiltekins notanda.
- Til að bíða áður en prófunin hefst geturðu skilgreint hlé á flipanum **Almennt** í Excel-færibreytuskránni. Þetta hlé má nota í runuvinnslu (til dæmis ef keyra þarf verkflæði áður en hægt er að framkvæma næsta skref.)

## <a name="advanced-scripting"></a>Ítarlegri forskriftir

### <a name="cli"></a>CLI

Hægt er að kalla RSAT úr glugganum **Skipanakvaðning** eða **PowerShell**.

> [!NOTE]
> Staðfestu að umhverfisbreytan **TestRoot** sé stillt á RSAT-uppsetningarslóðina. (Í Microsoft Windows skaltu opna **Stjórnborð**, velja **Kerfi og öryggi \> Kerfi \> Ítarlegir kerfisstillingar** og velja síðan **Umhverfisbreytur** .)

1. Opnaðu gluggann **Skipanakvaðning** eða **PowerShell** sem stjórnandi.
2. Farðu í RSAT uppsetningarskrána.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Listi yfir alla skipanir.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Sýnir hjálp um allar tiltækar skipanir og færibreytur þeirra.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Valkvæðar færibreytur

`command`: Þar sem ``[command]`` er ein af skipununum sem tilgreindar eru hér að neðan.

#### <a name="about"></a>um

Birtir núverandi útgáfu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Hreinsar skjáinn.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>sækja

Sækir viðhengi fyrir tilgreint prófatilfelli í úttaksskrána.
Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik. Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>niðurhal: nauðsynlegar færibreytur

+ `test_case_id`: Stendur fyrir kenni prófunardæmis.
+ `output_dir`: Stendur fyrir skráasafn úttaks. Skráasafnið verður að vera til.

##### <a name="download-examples"></a>niðurhal: dæmi

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>breyta

Gerir þér kleift að opna færibreytuskrá í Excel-forritinu og breyta henni.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>breyta: nauðsynlegar færibreytur

+ `excel_file`: Verður að innihalda fulla slóð á fyrirliggjandi Excel-skrá.

##### <a name="edit-examples"></a>breyta: dæmi

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Myndar prófaframkvæmdar- og færibreytuskrár fyrir tilgreint próftilfelli í úttaksskráasafninu. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik. Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>mynda: nauðsynlegar færibreytur

+ `test_case_id`: Stendur fyrir kenni prófunardæmis.
+ `output_dir`: Stendur fyrir skráasafn úttaks. Skráasafnið verður að vera til.

##### <a name="generate-examples"></a>mynda: dæmi

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

Býr til nýtt prófatilvik, unnið úr gefnu prófatilviki. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik. Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: nauðsynlegar færibreytur

+ `parent_test_case_id`: Stendur fyrir kenni yfirprófunardæmis.
+ `test_plan_id`: Stendur fyrir kenni prófunaráætlunar.
+ `test_suite_id`: Stendur fyrir kenni prófunarpakka.

##### <a name="generatederived-examples"></a>generatederived: dæmi

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Myndar aðeins prófunarframkvæmdarskrá fyrir tilgreint prófunartilfelli í úttaksskráasafninu. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik. Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: nauðsynlegar færibreytur

+ `test_case_id`: Stendur fyrir kenni prófunardæmis.
+ `output_dir`: Stendur fyrir skráasafn úttaks. Skráasafnið verður að vera til.

##### <a name="generatetestonly-examples"></a>generatetestonly: dæmi

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

Býr til öll prófunartilvik fyrir tilgreindan flokk í úttaksskráasafninu. Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka. Notaðu eitthvert gildi úr dálknum sem færibreytuna **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: nauðsynlegar færibreytur

+ `test_suite_name`: Stendur fyrir heiti prófunarpakka.
+ `output_dir`: Stendur fyrir skráasafn úttaks. Skráasafnið verður að vera til.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: dæmi

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>help

Eins og [?](#section) skipun.

#### <a name="list"></a>Listi

Listar yfir öll tiltæk prófunartilvik.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Listar yfir allar tiltækar prófunaráætlanir.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Listar yfir prófunartilvik fyrir tilgreindan prófunarflokk. Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka. Notaðu eitthvert gildi úr fyrsta dálknum sem færibreytuna **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: nauðsynlegar færibreytur

+ `suite_name`: Heiti æskilegs pakka.

##### <a name="listtestsuite-examples"></a>listtestsuite: dæmi

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Listar yfir alla tiltæka prófunarflokka.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Spilar prófunartilvik með Excel-skrá.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>playback: nauðsynlegar færibreytur

+ `excel_file`: Full slóð að Excel-skránni. Skrá verður að vera til.

##### <a name="playback-examples"></a>spilun: dæmi

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Spilar mörg prófunartilvik í einu. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik. Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playback: nauðsynlegar færibreytur

+ `test_case_id1`: kenni fyrirliggjand prófunardæmis.
+ `test_case_id2`: kenni fyrirliggjand prófunardæmis.
+ `test_case_idN`: kenni fyrirliggjand prófunardæmis.

##### <a name="playbackbyid-examples"></a>playbackbyid: dæmi

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Spilar mörg prófunartilvik í einu með Excel-skrám.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany: nauðsynlegar færibreytur

+ `excel_file1`: Full slóð að Excel-skránni. Skrá verður að vera til.
+ `excel_file2`: Full slóð að Excel-skránni. Skrá verður að vera til.
+ `excel_fileN`: Full slóð að Excel-skránni. Skrá verður að vera til.

##### <a name="playbackmany-examples"></a>playbackmany: dæmi

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Spilar öll prófunartilvik úr tilgreinda prófunarflokknum.
Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka. Notaðu eitthvert gildi úr fyrsta dálknum sem færibreytuna **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: nauðsynlegar færibreytur

+ `suite_name`: Heiti æskilegs pakka.

##### <a name="playbacksuite-examples"></a>playbacksuite: dæmi

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>quit

Lokar forritinu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>upload

Hleður inn öllum skrám sem tilheyra tilgreindum prófunarflokk eða prófunartilvikum.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>upphal: nauðsynlegar færibreytur

+ `suite_name`: Allar skrár sem tilheyra tilgreindum prófunarpakka verður hlaðið upp.
+ `testcase_id`: Allar skrár sem tilheyra tilgreindu prófunardæmi verður hlaðið upp.

##### <a name="upload-examples"></a>hlaða upp: dæmi

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Hleður aðeins inn upptökuskránni sem tilheyrir tilgreindum prófunartilvikum.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: nauðsynlegar færibreytur

+ `testcase_id`: Upptökuskrá sem tilheyrir tilgreindum prófunarpökkum verður hlaðið upp.

##### <a name="uploadrecording-examples"></a>uploadrecording: dæmi

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Sýnir tvær leiðir til að kalla á þetta forrit: önnur sem notar sjálfgefna stillingaskrá og önnur með stillingarskrá.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>Windows PowerShell-dæmi

#### <a name="run-a-test-case-in-a-loop"></a>Keyrðu prófunardæmi í lykkju

Þú ert með prófunarforskrift sem stofnar nýjan viðskiptavin. Með forskriftum er hægt að keyra þetta prófunardæmi í lykkju með slembiröðun á eftirfarandi gögnum áður en hver ítrekun er keyrð:

- Kenni viðskiptavinar
- Nafn viðskiptavinar
- Aðsetur viðskiptavinar

Viðskiptavinakennið verður á sniðinu *ATCUS\<number\>* þar sem \<number\> er gildi á milli **000000001** og **999999999**.

Eftirfarandi dæmi notar eina breytu, **byrja**, til að skilgreina fyrsta númerið sem er notað. Er notuð önnur færibreyta, **nr**, til að skilgreina fjölda viðskiptavina sem verður að stofna. Fyrir hverja ítrekun er færibreytunum í Excel-færibreytuskránni breytt með því að nota virknina UpdateCustomer. Síðan er RSAT-skipanalínan kölluð í virkninni RunTestCase.

Opnaðu Microsoft Windows PowerShell Integrated Scripting Environment (ISE) í stjórnandaham og límdu eftirfarandi kóða inn í gluggann sem heitir **Untitled1.ps1**.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Keyrðu handrit sem fer eftir gögnum í Microsoft Dynamics 365

Eftirfarandi dæmi notar Open Data Protocol (OData)-kall til að finna pöntunarstöðu innkaupapöntunar. Ef staðan er ekki **innheimt**, getur þú til dæmis kallað í RSAT-prófunardæmi sem bókar reikninginn.

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]