---
title: Nota kennslu fyrir Regression Suite Automation Tool
description: Þetta efni sýnir hvernig á að nota Regression Suite Automation Tool (RSAT). Það lýsir ýmsum eiginleikum og gefur dæmi sem nota ítarlegar forskriftir.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: cf3ca501efb4e540994b01e651eee5b8aab4ddbc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191087"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Notaðu kennsluefni fyrir Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Notaðu verkfæri þín í internetvafranum til að sækja og vista þessa síðu á pdf-sniði. 

Þetta kennsluefni fer í gegnum nokkra ítarlega eiginleika Regression Suite Automation Tool (RSAT), inniheldur sýniúthlutun og lýsir stefnu og lykilatriðum.

## <a name="features-of-rsattask-recorder"></a>Eiginleikar RSAT/verkskráningar

### <a name="validate-a-field-value"></a>Villuleita reitargildi

Nánari upplýsingar um þennan eiginleika er að finna í [Stofna nýja verkskráningu sem hefur staðfestingaraðgerð](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Vistuð breyta

Nánari upplýsingar um þennan eiginleika er að finna í [Breyta núverandi verkskráningu til að búa til vistað breytu](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Afleitt prófunardæmi

1. Opnaðu Regression Suite Automation Tool (RSAT) og veldu bæði prófunardæmin sem þú stofnaðir í [Setja upp Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).
2. Veldu **Nýtt \> Stofna afleitt prófunardæmi**.

    ![Stofna afleidda prófunardæmisskipun í valmyndinni Nýtt](./media/use_rsa_tool_01.png)

3. Þú færð skilaboð sem kveða á um að stofnað verði prófunardæmi fyrir hvert valið prófunardæmi í núverandi prófunarpakka og að hvert afleidd prófunardæmi muni hafa eigið afrit af Excel-færibreytuskránni. Veljið **Í lagi**.

    > [!NOTE]
    > Þegar þú keyrir afleidd prófunardæmi notar það verkskráningu yfirprófunardæmis og eigið afrit af Excel-færibreytuskránni. Þannig geturðu keyrt sama prófið með mismunandi færibreytum, án þess að þurfa að viðhalda fleiri en einni verkskráningu. Afleitt prófunardæmi þarf ekki að vera hluti af sama prófunarpakka og yfirprófunardæmið.

    ![Skilaboðagluggi](./media/use_rsa_tool_02.png)

    Tvö afleidd prófunardæmi eru stofnuð og hakreiturinn **Afleidd?** er valinn fyrir þau.

    ![Afleidd prófunardæmi stofnuð](./media/use_rsa_tool_03.png)

    Afleidd prófunardæmi eru sjálfvirkt stofnuð í Azure DevOps. Það er undiratriði í prófunardæminu **Stofna nýja afurð** og er merkt með sérstöku lykilorði: **RSAT: DerivedTestSteps**. Þessum prófunardæmum er einnig sjálfkrafa bætt við prófunaráætlunina í Azure DevOps.

    ![Lykilorðið RSAT: DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Ef afleidd prófunardæmi sem eru af einhverjum ástæðum stofnuð eru ekki í réttri röð, skaltu fara í Azure DevOps og endurraða prófdæmunum í prófunarpakkanum, þannig að RSAT geti keyrt þau í réttri röð.

4. Veldu aðeins afleidd prófunardæmi og veldu síðan **Breyta** til að opna samsvarandi Excel-færibreytuskrár.
5. Breyttu þessum Excel-færibreytuskrám á sama hátt og þú breyttir yfirskránum. Með öðrum orðum skaltu ganga úr skugga um að afurðakennið sé stillt þannig að það sé sjálfkrafa myndað. Passaðu einnig að vistuð breyta sé afrituð í viðeigandi reiti.
6. Á flipanum **Almennt** í báðum Excel-færibreytuskránum skaltu uppfæra gildi reitsins **Fyrirtæki** í **USSI**, þannig að afleidd prófunardæmi verði keyrð gegn öðrum lögaðila en yfirprófunardæmið. Til að keyra prófdæmin gegn ákveðnum notanda (eða hlutverki sem tengist ákveðnum notanda) getur þú uppfært gildi reitsins **Prófa notanda**.
7. Veldu **Keyra** og sannreyndu að afurðin sé stofnuð bæði í USMF-lögaðilanum og USSI-lögaðilanum.

### <a name="validate-notifications"></a>Sannprófa tilkynningar

Þennan eiginleika er hægt að nota til að staðfesta hvort aðgerð hafi átt sér stað. Til dæmis, þegar framleiðslupöntun er stofnuð, áætluð og síðan hafin sýnir forritið skilaboðin „Production - Start“ til að tilkynna þér að framleiðslupöntun hafi verið hafin.

![Framleiðsla – Ræsa tilkynningu](./media/use_rsa_tool_05.png)

Þú getur valið þessi skilaboð í gegnum RSAT með því að slá inn skilaboðartexta á flipann **MessageValidation** í Excel-færibreytuskránni fyrir viðeigandi skráningu.

![Flipinn Sannprófun skilaboða](./media/use_rsa_tool_06.png)

Þegar prófunardæmið hefur verið keyrt eru skilaboðin í Excel-færibreytuskránni borin saman við skilaboðin sem birtast. Ef skilaboðin stemma ekki mun prófunardæmið ekki takast.

> [!NOTE]
> Þú getur slegið inn fleiri en eina skilaboð á flipann **MessageValidation** í Excel-færibreytuskránni. Skilaboðin geta einnig verið villuboð eða viðvörunarboð í stað upplýsingaboða.

### <a name="validate-values-by-using-operators"></a>Staðfesta gildi með því að nota virkja

Í fyrri útgáfum af RSAT var aðeins hægt að sannprófa gildi ef eftirlitsgildi jafngild áætluðu gildi. Hinn nýi eiginleiki gerir þér kleift að staðfesta að breyta sé ekki jafnt og, sé minna en eða meira en tilgreint gildi.

- Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    Í Excel-færibreytuskránni birtist nýi reiturinn **Virki**.

    > [!NOTE]
    > Ef þú hefur verið að nota eldri útgáfu af RSAT verður þú að búa til nýjar Excel-færibreytuskrár.

    ![Reiturinn Virki](./media/use_rsa_tool_07.png)

Eftirfarandi dæmi sýnir hvernig hægt er að nota þennan eiginleika til að sannreyna hvort lagerbirgðir séu meiri en 0 (núll).

1. Í kynningargögnum í fyrirtækinu **USMF** skaltu stofna verkskráningu sem er með eftirfarandi skref:

    1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
    2. Nota flýtiafmörkun til að finna færslur Til dæmis sía gildið í reitnum **1000** fyrir reitinn **Vörunúmer**.
    3. Veldu **Lagerbirgðir**.
    4. Nota flýtiafmörkun til að finna færslur Til dæmis, sía á gildinu **1** fyrir reitinn **Vefsvæði**.
    5. Í listanum skal merkja valda línu.
    6. Sannprófaðu að gildi reitsins **Samtals magn til ráðstöfunar** sé **411,0000000000000000**.

2. Vistaðu verkskráninguna í BPM-safnið í LCS og samstilltu það við Azure DevOps.
3. Bættu prófunardæminu við prófunaráætlunina og settu prófunardæmið í RSAT.
4. Opnaðu Excel-færibreytuskrána. Á flipanum **InventOnhandItem** muntu sjá hlutann **Staðfesta InventOnhandItem** sem inniheldur reitinn **Virki**.

    ![Reiturinn Virki](./media/use_rsa_tool_08.png)

5. Til að sannreyna hvort birgðir á lager verði alltaf meiri en 0 skaltu breyta gildi reitsins **Gildi** úr **411** í **0** og gildi reitsins **Virki** úr samasemmerki (**=**) í meiraenmerki (**\>**).

    ![Gildum reitanna Gildi og Virki breytt](./media/use_rsa_tool_09.png)

6. Vistaðu og lokaðu Excel-færibreytskránni.
7. Veldu **Hlaða upp** til að vista breytingarnar sem þú gerðir í Excel-færibreytuskránni í Azure DevOps.

Nú, ef gildi reitsins **Samtals magn til ráðstöfunar** fyrir tilgreint atriði í birgðum er meira en 0 (núll), prófanir munu standast, óháð raunverulegu gildi lagerbirgða.

### <a name="generator-logs"></a>Kladdar skýrslugerðar

Þessi eiginleiki býr til möppu sem inniheldur kladdana í prófunardæmunum sem hafa verið keyrð.

- Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.

    ```
    <add key="LogGeneration" value="false" />
    ```

Þegar prófunardæmin hafa verið keyrð geturðu fundið kladdaskrárnar undir **C:\\Notendur\\\<Notendanafn\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![Mappan GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> Ef það voru til staðar prófunardæmi áður en þú breyttir gildinu í .config-skránni verða kladdar ekki myndaðir fyrir þessi prófdæmi fyrr en þú myndar nýjar prófunarkeyrsluskrár.
> 
> ![Skipunin Mynda textakeyrsluskrár í valmyndinni Nýtt](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Skyndimynd

Þessi eiginleiki tekur skjámyndir af þeim skrefum sem voru gerð meðan á verkskráningu stóð.

- Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Undir **C:\\Notendur\\\<Notendanafn\>\\AppData\\Roaming\\regressionTool\\playback**, sérstakri möppu er stofnuð fyrir hvert prófunardæmi sem er keyrt.

![Mappan Skyndimynd fyrir prófunardæmi](./media/use_rsa_tool_12.png)

Í sérhverri af þessum möppum er hægt að finna skyndimyndir af þeim skrefum sem voru gerð meðan prófunardæmin voru keyrð.

![Skyndimyndaskrár](./media/use_rsa_tool_13.png)

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

![Flæði fyrir kynningaraðstæður](./media/use_rsa_tool_14.png)

Eftirfarandi mynd sýnir viðskiptaferlin fyrir þessar aðstæður í RSAT.

![Viðskiptaferli fyrir kynningaraðstæður](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Stjórnunarstefna – Lykilnám

### <a name="data"></a>Gögn

- Passaðu að þú hafir dæmigert gagnamagn (afrit af framleiðslu-/gullgrunnstillingargögnum auk yfirfærðra gagna).
- Þegar þú myndar ný gögn í gegnum verkskráningu skaltu stofna prófunarheiti sem munu ekki rekast á við fyrirliggjandi heiti (t.d. nota forskeyti eins og **RSATxxx**).
- Notaðu endurheimt Azure Point-In-Time til að endurkeyra prófanir í umhverfi sem ekki eru í 1. lagi.
- Þó að þú getir notað Excel-aðgerðirnar **RANDOM** og **NOW** til að mynda einkvæma samsetningu er framlagið tiltölulega hátt. Eftirfarandi er dæmi.

    ```
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

### <a name="command-line"></a>Skipunarlína

Hægt er að kalla RSAT úr glugganum **Skipanakvaðning**.

> [!NOTE]
> Staðfestu að umhverfisbreytan **TestRoot** sé stillt á RSAT-uppsetningarslóðina. (Í Microsoft Windows skaltu opna **Stjórnborð**, velja **Kerfi og öryggi \> Kerfi \> Ítarlegir kerfisstillingar** og velja síðan **Umhverfisbreytur** .)

1. Opnaðu gluggann **Skipanakvaðning** sem stjórnandi.
2. Keyrðu verkfærið úr skráarsafni uppsetningar.

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Listi yfir alla skipanir.

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>Windows PowerShell-dæmi

#### <a name="run-a-test-case-in-a-loop"></a>Keyrðu prófunardæmi í lykkju

Þú ert með prófunarforskrift sem stofnar nýjan viðskiptavin. Með forskriftum er hægt að keyra þetta prófunardæmi í lykkju með slembiröðun á eftirfarandi gögnum áður en hver ítrekun er keyrð:

- Kenni viðskiptavinar
- Nafn viðskiptavinar
- Aðsetur viðskiptavinar

Kenni viðskiptavinar verður á sniðinu *ATCUS\<númer\>*, þar sem \<númer\> er gildi á milli **000000001** og **999999999**.

Eftirfarandi dæmi notar eina breytu, **byrja**, til að skilgreina fyrsta númerið sem er notað. Er notuð önnur færibreyta, **nr**, til að skilgreina fjölda viðskiptavina sem verður að stofna. Fyrir hverja ítrekun er færibreytunum í Excel-færibreytuskránni breytt með því að nota virknina UpdateCustomer. Síðan er RSAT-skipanalínan kölluð í virkninni RunTestCase.

Opnaðu Microsoft Windows PowerShell Integrated Scripting Environment (ISE) í stjórnandaham og límdu eftirfarandi kóða inn í gluggann sem heitir **Untitled1.ps1**.

```
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
$excelFilename = "full path to excel file parameter file"
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

```
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
