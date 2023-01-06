---
title: Regression Suite Automation Tool kennsla
description: Þessi grein sýnir hvernig á að nota Regression Suite Automation Tool (RSAT). Það lýsir ýmsum eiginleikum og gefur dæmi sem nota ítarlegar forskriftir.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a270398ddebef0f47a2c31b0ffb022e3df6489c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277405"
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

- Til að nota þennan eiginleika á meðan RSAT er keyrt með notandaviðmóti skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Til að nota þennan eiginleika á meðan RSAT er keyrt af CLI (til dæmis Azure DevOps) skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Þegar þú keyrir prófunartilvikin mun RSAT búa til myndatökur (myndir) af skrefunum og vista þær í spilunarmöppu prófatilvikanna í vinnuskránni. Í afspilunarmöppunni er búin til sérstök undirmappa sem heitir **StepSnapshots**. Þessi mappa inniheldur skyndimyndir fyrir prófunartilvikin sem eru keyrð.

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Sýnir allar skipanir eða sýnir hjálp fyrir tiltekna skipun ásamt tiltækum færibreytum.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Valkvæðar færibreytur

`command`: Þar sem ``[command]`` er ein af skipununum í listanum á undan.

#### <a name="about"></a>um

Birtir útgáfu uppsetts RSAT.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Hreinsar skjáinn.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>sækja

Sækir viðhengi (skráningar-, framkvæmda- og færibreytuskrár) fyrir tilgreint próftilfelli ú Azure DevOps í úttaksskráasafninu. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik og notað eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>niðurhal: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun niðurhalsferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.

##### <a name="download-required-parameters"></a>niðurhal: nauðsynlegar færibreytur

+ `test_case_id`: Stendur fyrir kenni prófunardæmis.

##### <a name="download-optional-parameters"></a>sækja: valkvæðar færibreytur

+ `output_dir`: Sýnir vinnsluskráasafn úttaksins. Skráasafnið verður að vera til. Vinnsluskráasafnið úr stillingunum verður notað ef þessi færibreyta er ekki tilgreind.

##### <a name="download-examples"></a>niðurhal: dæmi

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Sækir viðhengi (skráningar-, framkvæmda- og færibreytuskrár) fyrir öll próftilfelli í tilgreindum prófunarpakka úr Azure DevOps í úttaksskráasafninu. Þú getur notað skipunina ``listtestsuitenames`` til að fá öll tiltæk prófatilvik og notað hvaða gildi sem er sem færibreytuna **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun niðurhalsferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.
+ `/byid`: Þessi rofi gefur til kynna að æskilegur prófunarpakki sé auðkenndur með Azure DevOps-auðkenni sínu í stað heitis prófunarpakkans.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: nauðsynlegar færibreytur

+ `test_suite_name`: Stendur fyrir heiti prófunarpakka. Þessi færibreyta er nauðsynleg ef /byid-rofinn er **ekki** tilgreindur. Þetta heiti er heiti Azure DevOps-prófunarpakkans.
+ `test_suite_id`: Stendur fyrir kenni prófunarpakka. Þessi færibreyta er nauðsynleg ef /byid-rofinn **er** tilgreindur. Þetta auðkenni er auðkenni prófunarpakka Azure DevOps.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: valfrjálsar færibreytur

+ `output_dir`: Sýnir vinnsluskráasafn úttaksins. Skráasafnið verður að vera til. Vinnsluskráasafnið úr stillingunum verður notað ef þessi færibreyta er ekki tilgreind.

##### <a name="downloadsuite-examples"></a>downloadsuite: dæmi

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>breyta

Gerir þér kleift að opna færibreytuskrá í Excel-forritinu og breyta henni.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>breyta: nauðsynlegar færibreytur

+ `excel_file`: Verður að innihalda fulla slóð á fyrirliggjandi Excel-skrá.

##### <a name="edit-examples"></a>breyta: dæmi

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Myndar prófaframkvæmdar- og færibreytuskrár fyrir tilgreint próftilfelli í úttaksskráasafninu. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik. Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>búa til: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun vinnsluferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.
+ `/dllonly`: Búa til aðeins til keyrsluskrár prófunar. Ekki endurgera Excel-færibreytuskrána.
+ `/keepcustomexcel`: Uppfæra núverandi færibreytuskrá. Endurnýja einnig keyrsluskrár.

##### <a name="generate-required-parameters"></a>mynda: nauðsynlegar færibreytur

+ `test_case_id`: Stendur fyrir kenni prófunardæmis.

##### <a name="generate-optional-parameters"></a>mynda: valkvæðar færibreytur

+ `output_dir`: Sýnir vinnsluskráasafn úttaksins. Skráasafnið verður að vera til. Vinnsluskráasafnið úr stillingunum verður notað ef þessi færibreyta er ekki tilgreind.

##### <a name="generate-examples"></a>mynda: dæmi

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Býr til nýtt afleitt prófunartilvik (undireiningu prófunartilviks) fyrir uppgefið prófunartilvik. Nýja prófunartilvikið er einnig bætt við tilgreinda prófunarpakkann. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik og notað eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun vinnsluferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.

##### <a name="generatederived-required-parameters"></a>generatederived: nauðsynlegar færibreytur

+ `parent_test_case_id`: Stendur fyrir kenni yfirprófunardæmis.
+ `test_plan_id`: Stendur fyrir kenni prófunaráætlunar.
+ `test_suite_id`: Stendur fyrir kenni prófunarpakka.

##### <a name="generatederived-examples"></a>generatederived: dæmi

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Myndar aðeins prófunarframkvæmdarskrá fyrir tilgreint prófunartilfelli. Þetta myndar ekki Excel-færibreytuskrána Skrárnar eru búnar til í tilgreindu úttakssafni. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik og notað eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun vinnsluferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: nauðsynlegar færibreytur

+ `test_case_id`: Stendur fyrir kenni prófunardæmis.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: valkvæðar færibreytur

+ `output_dir`: Sýnir vinnsluskráasafn úttaksins. Skráasafnið verður að vera til. Vinnsluskráasafnið úr stillingunum verður notað ef þessi færibreyta er ekki tilgreind.

##### <a name="generatetestonly-examples"></a>generatetestonly: dæmi

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Býr til sjálfvirkniskrár prófunar fyrir öll prófunartilvik í tilgreindu prófunarsafni. Þú getur notað skipunina ``listtestsuitenames`` til að fá öll tiltæk prófatilvik og notað hvaða gildi sem er sem færibreytuna **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun vinnsluferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.
+ `/dllonly`: Búa til aðeins til keyrsluskrár prófunar. Ekki endurgera Excel-færibreytuskrána.
+ `/keepcustomexcel`: Uppfæra fyrirliggjandi færibreytuskrá. Endurnýja einnig keyrsluskrár.
+ `/byid`: Þessi rofi gefur til kynna að æskilegur prófunarpakki sé auðkenndur með Azure DevOps-auðkenni sínu í stað heitis prófunarpakkans.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: nauðsynlegar færibreytur

+ `test_suite_name`: Stendur fyrir heiti prófunarpakka. Þessi færibreyta er nauðsynleg ef /byid-rofinn er **ekki** tilgreindur. Þetta heiti er heiti Azure DevOps-prófunarpakkans.
+ `test_suite_id`: Stendur fyrir kenni prófunarpakka. Þessi færibreyta er nauðsynleg ef /byid-rofinn **er** tilgreindur. Þetta auðkenni er auðkenni prófunarpakka Azure DevOps.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: valkvæðar færibreytur

+ `output_dir`: Sýnir vinnsluskráasafn úttaksins. Skráasafnið verður að vera til. Vinnsluskráasafnið úr stillingunum verður notað ef þessi færibreyta er ekki tilgreind.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: dæmi

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>help

Eins og [?](#section) skipun.

#### <a name="list"></a>listi

Listar yfir öll tiltæk prófunartilvik í núverandi prófunaráætlun.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Listar yfir allar tiltækar prófunaráætlanir.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Listar yfir prófunartilvik fyrir tilgreindan prófunarflokk. Þú getur notað skipunina ``listtestsuitenames`` til að fá öll tiltæk prófunarsöfn og notað hvaða gildi sem er sem færibreytuna **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: nauðsynlegar færibreytur

+ `test_suite_name`: Heiti æskilegs pakka.

##### <a name="listtestsuite-examples"></a>listtestsuite: dæmi

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Listar yfir prófunartilvik fyrir tilgreindan prófunarflokk.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: nauðsynlegar færibreytur

+ `test_suite_id`: Kenni æskilegs pakka.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: dæmi

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Listar yfir alla tiltæka prófunarpakka í núverandi prófunaráætlun.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Spilar aftur prófunartilvikið sem tengist tilgreindri skrá Excel-færibreytu. Þessi skipun notar staðbundnar sjálfvirkniskrár og hleður ekki niður skrám frá Azure DevOps. Þessi skipun er ekki studd fyrir Commerce-prófanatilvik sölustaðar.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>spilun: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun spilunarferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.
+ `/comments[="comment"]`: Útvegaðu sérsniðinn upplýsingastreng sem er tekinn með í reitnum **Athugasemdir** á samantektar- og niðurstöðusíðum prófunar fyrir keyrslur Azure DevOps-prófana.

##### <a name="playback-required-parameters"></a>playback: nauðsynlegar færibreytur

+ `excel_parameter_file`: Full slóð á Excel breytuskrá. Skráin verður að vera til.

##### <a name="playback-examples"></a>spilun: dæmi

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Spilar mörg prófunartilvik í einu. Prófmálin eru auðkennd með auðkenni þeirra. Þessi skipun mun hlaða niður skrám frá Azure DevOps. Þú getur notað skipunina ``list`` til að fá öll tiltæk prófunartilvik og notað eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun spilunarferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.
+ `/comments[="comment"]`: Útvegaðu sérsniðinn upplýsingastreng sem er tekinn með í reitnum **Athugasemdir** á samantektar- og niðurstöðusíðum prófunar fyrir keyrslur Azure DevOps-prófana.

##### <a name="playbackbyid-required-parameters"></a>playback: nauðsynlegar færibreytur

+ `test_case_id1`: Kenni fyrirliggjandi prófunarmáls.
+ `test_case_id2`: Kenni fyrirliggjandi prófunarmáls.
+ `test_case_idN`: Kenni fyrirliggjandi prófunarmáls.

##### <a name="playbackbyid-examples"></a>playbackbyid: dæmi

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Spilar aftur í mörgum prófmálum á sama tíma. Prófunarmálin eru auðkennd með Excel-færibreytuskrám. Þessi skipun notar staðbundnar sjálfvirkniskrár og hleður ekki niður skrám frá Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun spilunarferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.
+ `/comments[="comment"]`: Útvegaðu sérsniðinn upplýsingastreng sem er tekinn með í reitnum **Athugasemdir** á samantektar- og niðurstöðusíðum prófunar fyrir keyrslur Azure DevOps-prófana.

##### <a name="playbackmany-required-parameters"></a>playbackmany: nauðsynlegar færibreytur

+ `excel_parameter_file1`: Full slóð á Excel breytuskrána. Skráin verður að vera til.
+ `excel_parameter_file2`: Full slóð á Excel breytuskrána. Skráin verður að vera til.
+ `excel_parameter_fileN`: Full slóð á Excel breytuskrána. Skráin verður að vera til.

##### <a name="playbackmany-examples"></a>playbackmany: dæmi

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Spilar öll prófunartilvik úr einum eða fleiri tilgreindum prófunarflokknum. Ef /staðbundinn skipting er tilgreind verða staðbundin viðhengi notuð fyrir spilun. Að öðrum kosti verða viðhengi sótt frá Azure DevOps. Þú getur notað skipunina ``listtestsuitenames`` til að fá öll tiltæk prófunarsöfn og notað hvaða gildi sem er úr fyrsta dálknum sem færibreytuna **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: valfrjálsir rofar

+ `/updatedriver`: Ef þessi rofi er tilgreindur, verður vefrekill netvafrans uppfærður eftir þörfum áður en spilunarferlið er keyrt.
+ `/local`: Þessi rofi gefur til kynna að staðbundin viðhengi ætti að nota fyrir spilun í stað þess að hlaða niður skrám frá Azure DevOps.
+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun spilunarferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.
+ `/comments[="comment"]`: Útvegaðu sérsniðinn upplýsingastreng sem er tekinn með í reitnum **Athugasemdir** á samantektar- og niðurstöðusíðum prófunar fyrir keyrslur Azure DevOps-prófana.
+ `/byid`: Þessi rofi gefur til kynna að æskilegur prófunarpakki sé auðkenndur með Azure DevOps-auðkenni sínu í stað heitis prófunarpakkans.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: nauðsynlegar færibreytur

+ `test_suite_name1`: Stendur fyrir heiti prófunarpakka. Þessi færibreyta er nauðsynleg ef /byid-rofinn er **ekki** tilgreindur. Þetta heiti er heiti Azure DevOps-prófunarpakkans.
+ `test_suite_nameN`: Stendur fyrir heiti prófunarpakka. Þessi færibreyta er nauðsynleg ef /byid-rofinn er **ekki** tilgreindur. Þetta heiti er heiti Azure DevOps-prófunarpakkans.
+ `test_suite_id1`: Stendur fyrir kenni prófunarpakka. Þessi færibreyta er nauðsynleg ef /byid-rofinn **er** tilgreindur. Þetta kenni er kenni Azure DevOps-prófunarpakkans.
+ `test_suite_idN`: Stendur fyrir kenni prófunarpakka. Þessi færibreyta er nauðsynleg ef /byid-rofinn **er** tilgreindur. Þetta kenni er kenni Azure DevOps-prófunarpakkans.

##### <a name="playbacksuite-examples"></a>playbacksuite: dæmi

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Keyrir öll prófunartilvik í tilgreindum Azure DevOps-prófunarpakka.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: valfrjálsir rofar

+ `/retry[=seconds]`: Ef þessi rofi er tilgreindur, og önnur RSAT tilvik loka fyrir prófunartilfelli, mun spilunarferlið bíða í tiltekinn fjölda sekúndna og reyna svo einu sinni enn. Sjálfgildið í \[sekúndum\] er 120 sekúndur. Án þessarar skiptingar verður hætt við ferlið strax ef prófunartilvik eru útilokuð.
+ `/comments[="comment"]`: Útvegaðu sérsniðinn upplýsingastreng sem er tekinn með í reitnum **Athugasemdir** á samantektar- og niðurstöðusíðum prófunar fyrir keyrslur Azure DevOps-prófana.
+ `/byid`: Þessi rofi gefur til kynna að æskilegur prófunarpakki sé auðkenndur með Azure DevOps-auðkenni sínu í stað heitis prófunarpakkans.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: nauðsynlegar færibreytur

+ `test_suite_id`: Stendur fyrir kenni prófunarpakka eins hann er í Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: dæmi

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>quit

Lokar forritinu. Þessi skipun er aðeins gagnleg þegar forritin eru keyrandi í gagnvirkri stillingu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>hætta: dæmi

`quit`

#### <a name="upload"></a>upload

Hleður upp viðhengisskrám (upptöku-, keyrslu- og færibreytuskrám) sem tilheyra tilteknu prófunarsafni eða prófunartilvikum í Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upphal: nauðsynlegar færibreytur

+ `test_suite_name`: Allar skrár sem tilheyra tilgreindum prófunarpakka verður hlaðið upp.
+ `test_case_id1`: Endurgera auðkenni fyrsta prófunartilfellis sem ætti að hlaða upp. Aðeins skal nota þessa færibreytu þegar ekkert heiti prófunarpakka hefur verið gefið upp.
+ `test_case_idN`: Endurgera auðkenni síðasta prófunartilfellis sem ætti að hlaða upp. Aðeins skal nota þessa færibreytu þegar ekkert heiti prófunarpakka hefur verið gefið upp.

##### <a name="upload-examples"></a>hlaða upp: dæmi

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Hleður aðeins upp þeirri skráningarskrá sem tilheyrir einu eða fleiri tilgreindum prófunartilvikum í Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: nauðsynlegar færibreytur

+ `test_case_id1`: Stendur fyrir auðkenni fyrsta prófunartilviksins fyrir skráninguna sem á að hlaða upp í Azure DevOps.
+ `test_case_idN`: Stendur fyrir auðkenni síðasta prófunartilviksins fyrir skráninguna sem á að hlaða upp í Azure DevOps.

##### <a name="uploadrecording-examples"></a>uploadrecording: dæmi

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Sýnir þrjá notkunarmáta þessa forrits.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Gagnvirk keyrsla forritsins:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Keyrsla forritsins með því að tilgreina skipun:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Keyra forritið með því að gefa upp stillingaskrá:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

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

```powershell
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
