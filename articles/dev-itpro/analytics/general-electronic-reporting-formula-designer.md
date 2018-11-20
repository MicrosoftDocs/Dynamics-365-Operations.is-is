---
title: "Formúluhönnuður í rafrænni skýrslugerð (ER)"
description: "Þessi Umfjöllunarefni útskýrir hvernig nota á formúluhönnuður í Rafræna skýrslugerð (ER)."
author: NickSelin
manager: AnnBe
ms.date: 10/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f0ded563ecf0b6d0ce67f046f631d8c4dcfc7802
ms.openlocfilehash: 1dc584355c8992ee701169fd5d29ad7b0300a498
ms.contentlocale: is-is
ms.lasthandoff: 10/22/2018

---

# <a name="formula-designer-in-electronic-reporting-er"></a>Formúluhönnuður í rafrænni skýrslugerð (ER)

[!include [banner](../includes/banner.md)]

Þessi Umfjöllunarefni útskýrir hvernig nota á formúluhönnuður í Rafræna skýrslugerð (ER). Þegar þú hannar snið fyrir tiltekið rafrænt skjal í ER má nota formúlur til að umbreyta gögnum þannig að þau uppfylli kröfur um gerð og snið skjalsins. Þessar formúlur líkjast formúlum í Microsoft Excel. Ýmsar tegundir aðgerða eru studdar í formúlunum: texti, dagsetning og tími, stærðfræðilegar, röklegar, upplýsingar, umbreyting á gagnagerð og annað (virkni sem er lénsértæk fyrir viðskipti).

## <a name="formula-designer-overview"></a>Yfirlit Formúluhönnuður.

Rafræn skýrslugerð styður formúluhönnuðinn. Á hönnunartíma er því hægt að skilgreina segðir sem hægt er að nota fyrir eftirfarandi verkefni á keyrslutíma:

- Umbreytingu gagna úr Microsoft Dynamics 365 for Finance and Operations gagnagrunninum sem eiga að vera slegin inn í gagnalíkan rafrænnar skýrslugerðar sem er hannað til að vera gagnagjafi fyrir snið rafrænnar skýrslugerðar. (Til dæmis geta þessar umbreytingar innihaldið síun, flokkun og umbreytingu gagnagerða.)
- Sníðing gagna sem verða að vera send á stofnað rafrænt skjal í samræmi við útlit og skilyrði tiltekins sniðs rafrænnar skýrslugerðar. (Til dæmis gæti sniðið verið gert í samræmi við viðkomandi tungumál eða menningu eða kóðunina).
- Stjórna ferlinu sem stofnar rafræn skjöl. (Til dæmis geta segðirnar virkjað eða slökkt á framleiðsla tiltekinna eininga sniðsins, fer eftir vinnslugögnum. Þær geta einnig truflað skráarmyndunarferlið eða sent skilaboð til notenda.)

Þú getur opnað síðu **Formúluhönnuðar** þegar þú framkvæmir einhvern af eftirfarandi aðgerðum:

- Bindingu gagnaveituvöru við þætti gagnalíkans.
- Bindingu gagnaveituvöru við þætti til að sníða.
- Alhliða viðhald reiknaðra svæða sem eru hluti af gagnagjöfum.
- Skilgreining sýnileikaskilyrða fyrir innsláttarfæribreytur notanda
- Hönnun á umbreytingum sniðsins
- Skilgreining á virkjun skilyrða fyrir þætti sniðsins.
- Skilgreining á skrárheiti fyrir FILE-þætti sniðsins.
- Skilgreining á skilyrðum fyrir villuleit ferlisstýringar.
- Skilgreining á texta í skilaboðum fyrir villuleit á ferlisstýringu.

## <a name="designing-er-formulas"></a>Hönnun á formúlum fyrir rafræna skýrslugerð

### <a name="data-binding"></a>gagnatengsl

Formúluhönnuður rafrænnar skýrslugerðar er hægt að nota til að skilgreina segð sem umbreytir gögnum sem eru móttekin frá gagnagjöfum, þannig að hægt sé að slá gögnin inn í gagnanotanda á keyrslutíma:

- Frá gagnagjöfum Finance and Operations og breytum keyrslutíma yfir í gagnlíkan rafrænnar skýrslugerðar
- Úr gagnalíkani rafrænnar skýrslugerðar yfir í snið rafrænnar skýrslugerðar.
- Frá gagnagjöfum Finance and Operations og breytum keyrslutíma yfir í snið rafrænnar skýrslugerðar

Eftirfarandi skýringarmynd sýnir hönnun segðar af þessari gerð. Í þessu dæmi námundar segðin gildin á **Intrastat.AmountMST** svæðinu Intrastat töflunni í Finance and Operations í tvo aukastafa og skilar síðan námunduðu gildi.

[![gagnatengsl](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Eftirfarandi mynd sýnir hvernig hægt er að nota segð af þessari gerð. Í þessu dæmi er niðurstaðan af hannaðri segð slegin inn í **Transaction.InvoicedAmount** hlutann af gagnalíkani **skattaskýrslulíkansins**.

[![Gagnatengsl notuð](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Við keyrslutíma námundar hannaða formúlan **ROUND (Intrastat.AmountMST, 2)** gildið á **AmountMST** svæðinu fyrir hverja færslu í Intrastat töflunni í tvo aukastafa. Hún slær þá inn námundaða gildið í **Transaction.InvoicedAmount** hlutann af gagnalíkani **skattaskýrslunnar**.

### <a name="data-formatting"></a>Gagnasnið

Formúluhönnuður ER hægt að nota til að skilgreina segð sem forsníður gögn sem er tekið úr gagnagjafa, þannig að gögn geta verið send sem hluti af myndandi rafrænu skjali. Þú gætir haft snið sem þarf að nota sem dæmigerða reglu sem þarf að endurnýta sem snið. Í þessu tilviki getur þú lagt sniðið fram einu sinni í skilgreiningu sniðs, sem nefnda umbreytingu sem hefur sniðsegð. Þessi nefnda umbreyting er síðan hægt að tengja við margar sniðseiningar þar sem úttakið verður að vera sniðið í samræmi við sniðsegðina sem þú bjóst til.

Eftirfarandi skýringarmynd sýnir hönnun umbreytingar sem samanstendur af þessari gerð. Í þessu dæmi styttir **TrimmedString** umbreytingin gögn á innleið af gagnagerðinni **Strengur** með því að fjarlægja bil fyrir framan og aftan. Hún skilar þá styttu strengagildi.

[![Umbreyting](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Eftirfarandi skýringarmynd sýnir hvernig er hægt að nota umbreyting af þessari gerð. Í þessu dæmi senda nokkrir þættir sniðs texta sem úttak til að búa til rafrænt skjal á keyrslutíma. Allir þessir sniðsþættir vísa til **TrimmedString** umbreytingar eftir heiti.

[![Umbreyting sem er notuð](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Þegar þættir sniðs, eins og **partyName** í ofangreindum myndum, vísa til **TrimmedString** umbreytingingarinnar, sendir umbreytingin texta sem úttak á rafrænu skjalinu. Þessi texti inniheldur ekki bil fyrir framan og aftan.

Ef þú ert með snið sem þarf að nota eitt og sér, getur þú sett fram það snið sem einstaka segð bindingar fyrir tiltekna sniðsþáttinn. Eftirfarandi skýringarmynd sýnir segð sem samanstendur af þessari gerð. Í þessu dæmi er **partyType** sniðsþáttur bundinn gagnagjafanum með segð sem breytir gögnum á innleið frá **Model.Company.RegistrationType** svæðinu í gagnagjafanum í hástafi. Segðin sendir þá texta sem úttak til rafræna skjalsins.

[![Sækja um snið fyrir einstaka þætti](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Vinnsla vinnsluflæðis

Formúluhönnuður rafrænnar skýrslugerðar er hægt að nota til að skilgreina segðir sem stýra vinnsluflæðinu við stofnun rafrænna skjala. Hægt er að framkvæma eftirfarandi verk:

- Skilgreina skilyrði til að ákvarða þegar þarf að stöðva ferli við myndun skjals
- Tilgreina segðir sem annað hvort búa til skilaboð fyrir notandann um stöðvuð ferli eða senda skilaboð aðgerðarskráningar um áframhaldandi ferli við myndun skýrslu.
- Tilgreina skráarnöfnin á stofnuðum rafrænum skjölum og stjórna skilyrðum fyrir stofnun þeirra.

Hverja reglu fyrir flæðistýringu ferlis er hannað sem einstaka villuleit. Eftirfarandi skýringarmynd sýnir sannvottun af þessari gerð. Hér er skýring á skilgreiningunni í þessu dæmi:

- Staðfestingin er metin þegar **INSTAT** hnúturinn á meðan XML-skráin er stofnuð.
- Það stöðvar aðgerðarferlið um leið og það skilar **FALSE** ef listi yfir færslur er tómur
- Sannvottunin skilar villuskilaboðum sem innihalda textann Finance and Operations merki SYS70894 á völdu tungumáli notanda.

[![Villuleit](./media/picture-validation.jpg)](./media/picture-validation.jpg)

Formúluhönnuður rafrænnar skýrslugerðar er einnig hægt að nota til að stofna skráarnafn fyrir stofnað rafrænt skjal og stjórna ferlinu fyrir stofnun skráa. Eftirfarandi skýringarmynd sýnir hönnun flæðistjórnunar ferlis sem samanstendur af þessari gerð. Hér er skýring á skilgreiningunni í þessu dæmi:

- Listi yfir færslur úr **model.Intrastat** gagnagjafanum er skipt í runur. Hver runa inniheldur allt að 1.000 færslur.
- Úttak býr til ZIP-skrá sem inniheldur eina skrá í xml-snið fyrir hverja runu sem var stofnuð.
- Segð skilar skráarnafni til að stofna rafræn skjöl með því að sameina skráarheiti og skráargerð. Fyrir aðra rönu og allar eftirfylgjandi runur inniheldur skráarheitið kenni runu sem nafnauka.
- Segð virkjar (með því að skila **TRUE**) ferli fyrir stofnun skráa fyrir runur sem innihalda að minnsta kosti eina færslu.

[![Skráarstýring](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Grunnmálskipan

Segðir rafrænnar skýrslugerðar geta innihaldið hverja sem er eða allar af eftirfarandi einingar:

- Fastagildi
- Stjórnendur
- Tilvísanir
- Slóðir
- Aðgerðir

#### <a name="constants"></a>Fastagildi

Þegar þú hannar segð getur þú notað texta og tölfræðilega fasta (það er gildi sem ekki er reiknað út). Til dæmis, tjáningin **VALUE ("100") + 20** notar tölulegt fastagildi **20** og fastagildi strengs **"100"**, og skilar tölulegu gildi **120**. Formúluhönnuður rafrænnar skýrslugerðar styður lausnarrunur. Þess vegna er hægt að tilgreina segðarstreng sem ætti að meðhöndla á annan hátt. Til dæmis, segðin **"Leo Tolstoy""War og Peace" "1 bindi"** skilar textastreng: **Leo Tolstoy "War og Peace" 1 bindi**

#### <a name="operators"></a>Virknitákn

Eftirfarandi tafla sýnir reikniaðgerðir sem þú getur notað til að gera grunn stærðfræðilegar aðgerðir, svo sem viðbót, frádráttur, margföldun og deiling.

| Virki | Merking               | Dæmi |
|----------|-----------------------|---------|
| +        | samlagning              | 1+2     |
| -        | Frádráttur Neitun | 5-2, -1 |
| \*       | Margföldun        | 7\*8    |
| /        | Skipting              | 9/3     |

Eftirfarandi tafla sýnir samanburðaraðgerðir sem eru studdar. Þú getur notað þessar aðgerðir til að bera saman tvö gildi.

| Virki | Merking                  | Dæmi    |
|----------|--------------------------|------------|
| =        | Jafnt                    | X=Y        |
| &gt;     | Stærra en             | X&gt;Y     |
| &lt;     | Minna en                | X&lt;Y     |
| &gt;=    | Stærra en eða jafnt og | X&gt;=Y    |
| &lt;=    | Minna en eða jafnt og    | X&lt;=Y    |
| &lt;&gt; | Er ekki jafnt og             | X&lt;&gt;Y |

Að auki er hægt að nota ampersand (&) sem textasambandsaðgerð. Þannig geturðu sameinað eða tengt saman einn eða fleiri textastrengi sem einn texta.

| Virki | Merking     | Dæmi                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Samtengja | "Ekkert til að prenta" & ":&nbsp;" & "engar skráningar fundust" |

##### <a name="operator-precedence"></a>Forgangsröðun stjórnanda

Röðin sem hlutar samsettrar segðar eru metnir á er mikilvæg. Til dæmis er niðurstaða segðarinnar **1 + 4/2** breytileg eftir því hvort samlagningaraðgerðin eða deilingaraðgerðin er fyrst framkvæmd. Hægt er að nota sviga til að skilgreina sérstaklega hvernig segð er metin. Til dæmis, til að gefa til kynna að samlagningaraðgerðin skuli gerð fyrst, getur þú breytt fyrri segðinni í **(1 + 4) / 2**. Ef þú gefur ekki skýrt til kynna röð aðgerða í segð er röðin byggð á sjálfgefna forgangi sem er úthlutað til undiraðgerðanna. Eftirfarandi tafla sýnir forgang sem er úthlutað hverri aðgerð. Aðgerðir sem hafa meiri forgang (til dæmis 7) eru metnir á undan aðgerðum sem hafa lægri forgang (til dæmis 1).

| Forgangur | Stjórnendur      | Málskipun                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Flokkun       | ( … )                                                                   |
| 6          | Aðgangur meðlima  | … . …                                                                   |
| 5          | Aðgerðakall  | … ( … )                                                                 |
| 4          | Margfaldandi | … \* …<br>… / …                                                         |
| 3          | Viðbótarefni       | … + …<br>… - …                                                          |
| 2          | Samanburður     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Aðgreining     | … , …                                                                   |

Ef segð felur í sér margar aðgerðir sem hafa sama forgang, eru þessar aðgerðir metnar frá vinstri til hægri. Til dæmis, skilar segðin **1 + 6 / 2 \* 3 &gt; 5** **true**. Við mælum með því að þú notar sviga til að tilgreina sérstaklega viðkomandi röð aðgerða í segðum, svo að segðirnar séu auðveldari að lesa og viðhalda.

#### <a name="references"></a>Tilvísanir

Öll gagnasöfn í núverandi hluta rafrænnar skýrslugerðar sem eru tiltækar við hönnun segðar geta verið notaðir sem tilvísanir með heiti. (Núverandi hluti rafrænnar skýrslugerðar getur verið annaðhvort líkan eða snið.) Til dæmis inniheldur núverandi gagnalíkan rafrænnar skýrslugerðar **ReportingDate** gagnagjafa og þessi gagnagjafi skilar gildi **DATETIME** gagnagerðarinnar. Til að forsníða þetta gildi á réttan hátt í skjalinu sem er búið til geturðu vísað til gagnagjafans í segðinni sem **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**.

Allir stafir í heiti á tilvísandi gagnagjafa sem ekki tákna staf í stafrófinu skulu hafa einfaldar gæsalappir (') fyrir framan. Ef heitið á tilvísandi gagnagjafa inniheldur að minnsta kosti eitt tákn sem ekki táknar stafina í stafrófinu, skal nafnið vera fyrir innan einfaldra gæsalappa. (Til dæmis geta þessi tákn sem eru ekki í stafrófinu verið greinarmerki eða önnur skrifuð tákn.) Hér eru nokkur dæmi:

- Gagnagjafinn **Dagsetning og tími í dag** verður að vera vísað í segð rafrænnar skýrslugerðar sem **'Dagsetning & tími í dag'**.
- **Nafnið ()** aðferðin fyrir **Viðskiptavinir** gagnagrunninn verður að vísað í segð rafrænnar skýrslugerðar sem **Customers.name ()'**.

Ef aðferðir gagnagjafa Finance and Operations hafa breytur er eftirfarandi málskipan notuð til að kalla á þessar aðferðir:

- Ef **isLanguageRTL** aðferðin í gagnagjafa **Kerfisins** hefur **EN-US** færibreytu af gagnagerðinni **Strengur**, þá skal vísa þessari aðferð í segð rafrænnar skýrslugerðar sem **System.'isLanguageRTL '("EN- US ")**.
- Tilvitnunarmerki eru ekki nauðsynleg þegar heiti aðferðar inniheldur aðeins tölustafatákn. Hins vegar er þeirra krafist fyrir töfluaðferð ef nafnið inniheldur sviga.

Þegar gagnagjafa **Kerfisins** er bætt við vörpun rafrænnar skýrslugerðar sem vísar til **Altækrar** notkunar á Finance and Operations klasanum, skilar segðin Boolean gildi **FALSE**. Breytta segðin **System.'isLanguageRTL '("AR")** skilar Boolean gildi **TRUE**.

Þú getur takmarkað hvernig þessi gildi eru samþykkt í breytur fyrir aðferð af þessari gerð:

- Aðeins fastar geta verið notaðir í aðferðum af þessari gerð. Gildi fastanna eru skilgreind á hönnunartíma.
- Aðeins frumstæðar (grunn) gagnagerðir eru studdar fyrir breytur af þessu tagi. (Frumstæðu gögnin eru heiltala, rauntala, Boolean, strengur og svo framvegis).

#### <a name="paths"></a>Slóðir

Þegar segð vísar í skipulögð gagnagjafa, geturðu nota skilgreiningu slóðar til að velja tiltekna frumstæðar einingu þess gagnagjafa. Stafurinn punktur (.) er notuð til að aðskilja einstakar einingar skipulagðs gagnagjafa. Til dæmis, núverandi gagnalíkan rafrænnar skýrslugerðar inniheldur **InvoiceTransactions** gagnagjafa og þessi gögn skila lista yfir færslur. Uppsetningin **InvoiceTransactions** inniheldur **AmountDebit** og **AmountCredit** svæðin og bæði svæðin skila tölugildum. Hægt er að hanna tjáningu til að reikna út reikningsfærða upphæð sem hér segir: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Aðgerðir

Næsta hluta er fjallað um aðgerðir sem hægt er að nota í segðum rafrænnar skýrslugerðar. Allir gagnagjafar segðarsamhengis (núverandi gagnalíkan rafrænnar skýrslugerðar eða snið rafrænnar skýrslugerðar) er hægt að nota sem breytur kallaðgerða, í samræmi við lista yfir frumbreytur fyrir kallaðgerðir. Fastar geta einnig verið notaðir sem breytur kallaðgerða. Til dæmis, núverandi gagnalíkan rafrænnar skýrslugerðar inniheldur **InvoiceTransactions** gagnagjafa og þessi gögn skila lista yfir færslur. Uppsetningin **InvoiceTransactions** inniheldur **AmountDebit** og **AmountCredit** svæðin og bæði svæðin skila tölugildum. Þar af leiðandi er hægt að hanna tjáningu til að reikna út reikningsfærða upphæð sem notar innbyggða námundunaraðgerð rafrænnar skýrslugerðar: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Studdar aðgerðir

Eftirfarandi töflur útskýrir eiginleika fyrir breytingar á gögnum sem eru tiltækar fyrir hönnun á gagnalíkön rafrænnar skýrslugerðar og skýrslur rafrænnar skýrslugerðar. Listi yfir aðgerðir er ekki fastur. Hönnuðir geta bætt við hann. Til að sjá lista yfir aðgerðir sem þú getur notað skaltu opna aðgerðargluggann í formúluhönnuði rafrænnar skýrslugerðar.

### <a name="date-and-time-functions"></a>Dagsetningar og tímavirkni

| Aðgerð | Lýsing | Dæmi |
|----------|-------------|---------|
| ADDDAYS (dagsetning og tími, dagar) | Bætir tilgreindum fjölda daga við tilgreint gildi dagsetningar / tíma. | **ADDDAYS (NOW(), 7)** skilar dagsetning og tími sjö daga fram í tímann. |
| DATETODATETIME (dagsetning) | Breytir tilgreindum dagsetningargildum í dagsetningu / tíma. | **DATETODATETIME (CompInfo. "GetCurrentDate () ')** skilar núverandi setudagsetningu Finance and Operations, desember 24, 2015, sem **12/24/2015 12:00:00 fyrir hádegi**. Í þessu dæmi er **CompInfo** gagnagjafi rafrænnar skýrslugerðar fyrir **Finance and Operations/tafla** gerð og vísar til CompanyInfo töflunni. |
| NOW () | Skilar núverandi dagsetningu og tíma hugbúnaðarþjóns Finance and Operations og gildi tíma sem dagsetningu/tíma. | |
| TODAY () | Skila gildandi dagsetningu og tíma netþjóns Finance and Operations sem dagsetningargildi. | |
| NULLDATE () | Skilar gagnagildi með **núlli**. | |
| NULLDATETIME () | Skilar **núll** dagsetningu / tíma gildi. | |
| DATETIMEFORMAT (datetime, format) | Breytir tilgreindri dagsetningu / tíma gildi í streng á tilgreindu sniði. (Fyrir upplýsingar um studd snið sjá [staðlað](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW (), "dd-mm-áááá")** skilar núverandi dagsetningu hugbúnaðarþjóns Finance and Operations, 24. desember, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið. |
| DATETIMEFORMAT (datetime, format, culture) | Breytir tilgreindri dagsetningu / tíma gildi í streng í tilgreindum sniði og [menningu](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Fyrir upplýsingar um studd snið sjá [staðlað](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW (), "D", "de")** skilar núverandi dagsetningu hugbúnaðarþjóns Finance and Operations, desember 24, 2015, sem **"24.12.2015"**, miðað við valda þýska menningu. |
| SESSIONTODAY () | Skilar núverandi setudagsetningu Finance and Operations sem dagsetningargildi. | |
| SESSIONNOW () | Skilar núverandi setudagsetningu Finance and Operations og tíma sem dagsetningu/tíma. | |
| DATEFORMAT (dagsetning, snið) | Skilar streng með framsetningu tiltekinnar dagsetningu í tilgreint snið. | **DATEFORMAT (SESSIONTODAY (), "dd-mm-áááá")** skilar núverandi setudagsetningu Finance and Operations, desember 24, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið. |
| DATEFORMAT (dagsetning, snið, menning) | Umbreyta tilgreinda dagsetningargildi í streng á tilgreindu sniði og [menningu](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Fyrir upplýsingar um studd snið sjá [staðlað](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "D", "de")** skilar núverandi setudagsetningu Finance and Operations, desember 24, 2015, sem **"24.12.2015"**, miðað við valda þýska menningu. |
| DAYOFYEAR (dagsetning) | Skilar heiltölu sem sýnir fjölda daga milli 1. janúar og tilgreindrar dagsetningu. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** skilar **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** skilar **1**. |
| DAGAR (dagsetning 1, dagsetning 2) | Skilar fjölda daga milli fyrri tilgreindu dagsetningunni og seinni tilgreindu dagsetningunni. Skilar jákvæðu gildi þegar fyrsta dagsetningin er seinna en seinni dagsetningin, skilar **0** (núll) þegar fyrsta dagsetningin er jafngild annarri dagsetningu, eða skilar neikvæðu gildi þegar fyrsta dagsetningin er á undan seinni dagsetningunni. | **DAYS (TODAY (), DATEVALUE (DATETIMEFORMAT (ADDDAYS (NÚNA (), 1), "yyyyMMdd"), "yyyyMMdd"))** skilar **-1**. |

### <a name="data-conversion-functions"></a>Gagnaumbreytingarvirkni

| Aðgerð | lýsing | Dæmi |
|----------|-------------|---------|
| DATETODATETIME (dagsetning) | Breytir tilgreindum dagsetningargildum í dagsetningu / tíma. | **DATETODATETIME (CompInfo. "GetCurrentDate () ')** skilar núverandi setudagsetningu Finance and Operations, desember 24, 2015, sem **12/24/2015 12:00:00 fyrir hádegi**. Í þessu dæmi er **CompInfo** gagnagjafi rafrænnar skýrslugerðar fyrir **Finance and Operations/tafla** gerð og vísar til CompanyInfo töflunni. |
| DATEVALUE (strengur, snið) | Skilar framsetningu á dagsetningu á tilteknum streng í tilgreindu sniði. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** skilar dagsetning 21. desember 2016, byggt á tilgreindu sérsniðnu sniði og sjálfgefna **EN-US** menningu hugbúnaðar. |
| DATEVALUE (strengur, snið, menning) | Skilar framsetningu dagsetningar af tiltekins strengs í tilgreindum sniði og menningu. | **DATEVALUE ("21-Gen-2016", "dd-MMM-YYYY", "ÞAÐ")** skilar dagsetningunni 21. janúar 2016, byggt á tilgreindu sérsniðnu sniði og menningu. Hins vegar beitir **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** undantekningu til að upplýsa notandann um að tilgreindur strengur sé ekki viðurkenndur sem gild dagsetning. |
| DATETIMEVALUE (strengur, snið) | Skilar dagsetningu / tíma framsetning á tiltekins strengs í tilgreint snið. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh: mm: ss")** skilar 2:55:00 fyrir hádegi þann 21 desember 2016, byggt á tilgreindu sérsniðnu sniði og sjálfgefinni **EN-US** menningu hugbúnaðar. |
| DATETIMEVALUE (strengur, snið, menning) | Tilgreina dagsetningu / tíma sem sýnir tiltekinn streng í tilgreindu sniði og menningu. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-YYYY hh: mm: ss", "IT")** skilar 2:55:00 fyrir hádegi þann 21. desember 2016, byggt á tilgreindu sérsniðið snið og menning. Hins vegar beitir **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh: mm: ss", "EN-US")** undantekningu til að upplýsa notandann um að tilgreindur strengur sé ekki viðurkenndur sem gild dagsetning/tími. |

### <a name="list-functions"></a>Listavirkni

<table>
<thead>
<tr>
<th>Aðgerð</th>
<th>lýsing</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (input, length)</td>
<td>Skipta tilgreindum intaksstreng í undirstrengi, sem hvert um sig hefur tilgreinda lengd. Skila niðurstöðu sem nýja lista.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> skilar nýjum lista sem samanstendur af tveimur færslum sem eru með reit <strong>STRING</strong>. Reitur í fyrstu færslunni inniheldur texta <strong>&quot;abc&quot;</strong>, og reitur í önnur færsla inniheldur texta <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr>
<td>SPLIT (innsláttur, skiltákn)</td>
<td>Skiptu tilgreindum innsláttarstreng í undirstrengi, byggt á tilgreindu skiltákni.</td>
<td><strong>SPLIT (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> skilar nýjum lista sem samanstendur af þremur færslum sem hafa <strong>STRING</strong> reit. Reitur í fyrstu skrá inniheldur texta <strong>&quot;X&quot;</strong>, reitur í síðari færslunni inniheldur textann &quot;&nbsp;&quot;, og reitur í þriðju færslunni inniheldur textann <strong>&quot;y&quot;</strong>. Ef skiltáknið er tómt, er nýjum listi skilað sem samanstendur af einni færslu sem inniheldur <strong>STRING</strong> reit sem inniheldur innsláttartexta. Ef innslátturinn er tómur er nýjum tómum lista skilað.
Ef annað hvort innslátturinn eða skiltáknið er ótilgreind (núll) kemur forritaundantekning upp.</td>
</tr>
<tr>
<td>SPLITLIST (listi, númer)</td>
<td>Tilgreindur listi er skipt í runur sem hver inniheldur tilgreindan fjölda færslna. Skila niðurstöðu sem nýja lista yfir runur sem inniheldur eftirfarandi einingar:
<ul>
<li>Runur sem reglulegir listar (<strong>Gildi </strong> þáttur)</li>
<li>Núverandi rununúmer (<strong>BatchNumber</strong>þáttur)</li>
</ul>
</td>
<td>Í eftirfarandi mynd er gagnagjafi <strong>Lína</strong> búinn til sem færslulisti af þremur færslum. Þessi listi er skiptur í runur, sem hver um sig inniheldur allt að tvær færslur.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Eftirfarandi mynd sýnir hannað útlit sniðs. Í þessu sniðmáti eru tengsl við gagnagjafann <strong>Línur</strong> mynduð til að búa til úttak á XML sniði. Þessi útkoma kynnir einstaka hnúta fyrir hverja runu og færslurnar í henni.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (færsla 1 [, færsla 2, ...])</td>
<td>Skila nýjum lista sem er myndaður úr tilgreindum frumbreytum.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> skilar tóm færsla, þar sem listi yfir reiti inniheldur alla reiti <strong>MainData</strong> og <strong>OtherData</strong> skráningar lista.</td>
</tr>
<tr>
<td>LISTJOIN (listi 1, listi 2, ...)</td>
<td>Skila sameinuðum lista sem er myndaður úr listum úr tilgreindum frumbreytum.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> skilar lista yfir sex færslur, þar sem einn reitur af gagnagerðinni <strong>STRING</strong> inniheldur staka stafi.</td>
</tr>
<tr>
<td>ISEMPTY (listi)</td>
<td>Skilar <strong>TRUE</strong> ef tilgreind listi inniheldur engin atriði. Skila annars <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (listi)</td>
<td>Skila tómum lista með því að nota tilgreindan lista sem uppruna fyrir skipulag lista.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> skilar nýjum tómum lista sem hefur sömu uppbyggingu og listinn sem skilað er með <strong>SPLIT</strong> aðgerðinni.</td>
</tr>
<tr>
<td>FIRST (listi)</td>
<td>Skila fyrsta færslan af tilgreindum lista,ef að sú færsla er ekki tómt. Annars er beitt undantekningu.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (list)</td>
<td>Skila fyrsta færslan af tilgreindum lista,ef að sú færsla er ekki tómt. Annars skal skila <strong>núll</strong> færslu.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (list)</td>
<td>Skilar lista sem inniheldur aðeins fyrsta atriði tilgreinds lista.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (path)</td>
<td>Þessi aðgerð keyrir sem val í minni. Hún skilar nýjum útflöttum lista sem nær til allra atriða sem hafa samsvörun við tilgreinda slóð. Slóðin verður að vera skilgreind sem gild slóð gagnagjafa á einingu gagnagjafa með gögnum á formi færslulista. Gagnaeiningar eins og slóð strengs og dagsetning ætti að gefa upp villu í segðasmíði rafrænnar skýrslugerðar á tíma hönnunar.</td>
<td>Ef fært er inn <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> sem gagnaveita (DS), <strong>COUNT( ALLITEMS (DS.Value))</strong> skilar <strong>3</strong>.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (slóð)</td>
<td>Þessi aðgerð keyrir sem sameinuð SQL-fyrirspurn. Hún skilar nýjum útflöttum lista sem nær til allra atriða sem hafa samsvörun við tilgreinda slóð. Slóðin verður að vera skilgreind sem gild slóð gagnagjafa á einingu gagnagjafa af gagnagerð færslulista og hún verður að innihalda að minnsta kosti ein tengsl. Gagnaeiningar eins og slóð strengs og dagsetning ætti að gefa upp villu í segðasmíði rafrænnar skýrslugerðar á tíma hönnunar.</td>
<td>Skilgreindu eftirfarandi gagnagjafa í líkanavörpun þinni:
<ul>
<li><strong>CustInv</strong> (gerðin <strong>Töflufærslur</strong>) sem vísar til töflunnar CustInvoiceTable</li> 
<li><strong>FilteredInv</strong> (gerðin <strong>Útreiknaður reitur</strong>) sem inniheldur segðina <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong></li>
<li><strong>JourLines</strong> (gerðin <strong>Útreiknaður reitur</strong>) sem inniheldur segðina <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relation'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong></li>
</ul>
<p>Þegar þú keyrir líkanavörpun þína til að kalla á gagnagjafann <strong>JourLines</strong> keyrist eftirfarandi SQL-skipun:</p>
VELJA ... FRÁ CUSTINVOICETABLE T1 KROSSTENJGA CUSTINVOICEJOUR T2 KROSSTENGJA CUSTINVOICETRANS T3 ÞAR SEM...
</td>
</tr>
<tr>
<td>ORDERBY (listi [, segð 1, segð 2, …])</td>
<td>Skila tilgreindum lista eftir að hann hefur verið flokkaður samkvæmt tilgreindum frumbreytum. Þessi frumbreytur geta verið skilgreindar sem segðir.</td>
<td>Ef <strong>Lánardrottinn</strong> er stilltur sem gagnagjafi rafrænnar skýrslugerðar, sem vísar til VendTable borðinu, <strong>ORDERBY (Smásali, Vendors.'name () ')</strong> skilar lista af söluaðilum sem flokkaðar eftir nafni í hækkandi röð.</td>
</tr>
<tr>
<td>REVERSE (listi)</td>
<td>Skila tilgreindum lista í röð sem er afturábak.</td>
<td>Ef <strong>Lánardrottinn</strong> er stilltur sem gagnagjafi rafrænnar skýrslugerðar sem vísar til VendTable töflunnar, <strong>REVERSE (ORDERBY (Vendors, Vendors.'name () ')) )</strong> skilar lista yfir seljendur sem eru flokkaðar eftir nafni í lækkandi röð.</td>
</tr>
<tr>
<td>WHERE (listi, skilyrði)</td>
<td>Skilar tilgreindum lista eftir að hann hefur verið síaður í samræmi við tilgreind skilyrði. Tilgreint skilyrði er beitt á listann í minni. Þannig er <strong>WHERE</strong> virknin frábrugðin <strong>FILTER</strong> aðgerðinni.</td>
<td>Ef <strong>Lánardrottinn</strong> er stilltur sem gagnagjafi rafrænnar skýrslugerðar sem vísar til VendTable töflunnar, <strong>WHERE (Söluaðilar, Vendors.VendGroup = &quot;40&quot;)</strong> skilar lista yfir seljendur sem tilheyra söluhópi 40.</td>
</tr>
<tr>
<td>ENUMERATE (listi)</td>
<td>Skila nýjum lista sem samanstendur af tölusettur færslur tilgreinds lista, og sem birtir eftirfarandi einingar:
<ul>
<li>Tilgreindar listaskráningar sem reglulegur listi(<strong>Gildi </strong> þáttur)</li>
<li>Gildandi færsluvísir (<strong>Númer </strong>þáttur)</li>
</ul>
</td>
<td>Í eftirfarandi mynd er búinn til <strong>Tölusettur</strong> gagnagjafi sem tölusettur listi yfir færslur seljanda frá <strong>Lánardrottnum</strong> gagnagjafans sem vísar til VendTable töflunnar.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Eftirfarandi mynd sýnir sniðið. Í þessu sniði eru gagnatengsl mynduð til að búa til úttak á XML sniði. Þetta úttak kynnir einstaka söluaðila sem upptalda hnúta.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (listi)</td>
<td>Skila fjölda skráninga í tilgreindum lista, ef listinn er ekki tómur. Skila annars <strong>0</strong> (núll).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> skilar <strong>2</strong>, þar sem <strong>SPLIT</strong> aðgerð býr til lista sem samanstendur af tveimur færslum.</td>
</tr>
<tr>
<td>LISTOFFIELDS (slóð)</td>
<td>Skilar færslulista sem er búinn til úr frumbreytu af einni af eftirfarandi gerðum:
<ul>
<li>Tölusetning líkans</li>
<li>Tölusetning sniðs</li>
<li>Gámur</li>
</ul>
<p>Listinn sem er búinn til samanstendur af færslum sem hafa eftirfarandi svæði:</p>
<ul>
<li>Nafn</li>
<li>Merkimiði</li>
<li>lýsing</li>
</ul>
Á keyrslutíma skilar reitir <strong>Merkimiða</strong> og <strong>Lýsingar</strong> gildum sem eru byggð á stillingu tungumálasniðs.
</td>
<td>Í eftirfarandi mynd er kynnt upptalning í gagnalíkönum.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Eftirfarandi mynd sýnir þessar upplýsingar:</p>
<ul>
<li>Upptalning líkans er sett í skýrslu sem gagnagjafi.</li>
<li>Segð rafrænnar skýrslugerðar notar tölusetningarlíkanið sem breytu á <strong>LISTOFFIELDS</strong> aðgerðinni.</li>
<li>Gagnagjafi af gerðinni færslulisti er settur í skýrslu með því að nota stofnaða segð rafrænnar skýrslugerðar.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Eftirfarandi dæmi sýnir sniðseiningar rafrænnar skýrslugerðar sem eru bundin við gagnagjafa af gerðinni færslulisti sem var búin til með því að nota <strong>LISTOFFIELDS</strong> aðgerðina.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Byggt á tungumálastillingum á yfirsniðseiningum FILE og FOLDER, er þýddur texti fyrir merki og lýsingar sleginn inn sem úttak sniðs rafrænnar skýrslugerðar.</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (slóð, tungumál)</td>
<td>Skilar færslulista sem er búin til úr frumbreytu, svo sem tölusetningarlíkani, tölusetningarsniði eða geymis. Listinn sem er búinn til samanstendur af færslum sem hafa eftirfarandi svæði:
<ul>
<li>Nafn</li>
<li>Merkimiði</li>
<li>lýsing</li>
<li>Þýtt</li>
</ul>
Á keyrslutíma skila svæði <strong>Merkimiða</strong> og <strong>Lýsingar</strong> gildum sem eru byggð á tungumálastillingum sniðsins og tilgreint tungumál. <strong>Er þýtt</strong> svæðið gefur til kynna að svæði <strong>Merkimiða</strong> hafi verið þýtt yfir á tilgreint tungumál.
</td>
<td>Til dæmis notar þú <strong>Útreiknað svæði</strong> gagnagjafann til að stilla <strong>enumType_de</strong> og <strong>enumType_deCH</strong> gagnagjafa fyrir <strong>enumType</strong> gagnalíkan tölusetningar.
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>Í þessu tilfelli er hægt að nota eftirfarandi segð til að fá merkið á tölusetningargildinu á svissneskri þýsku, ef þessi þýðing er í boði. Ef svissnesk þýska þýðingin er ekki tiltæk er merkið á þýsku.</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (listanum, svæðisheiti, skiltákn)</td>
<td>Skilar streng sem samanstendur af samsettum gildum tiltekins svæðis úr tilgreindum lista. Gildin eru aðskilin með tilgreindri afmörkun.</td>
<td>Ef slegið er inn <strong>SKIPTA(&quot;abc&quot;, 1)</strong> sem gagnagjafa (DS), <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> skilar <strong>&quot;a-b-c&quot;</strong>.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (listanum, markgildi, uppruni marks)</td>
<td>Skipta tilgreindum lista í nýjan lista af undirlínur og skila niðurstöðum sem innihald færslulista. <strong>Viðmiðunarmörk</strong> breytu skilgreinir gildi marksins til að skipta upprunalistanum. Færibreyta <strong>upprunamarks</strong> skilgreinir skrefið sem heildarupphæðin er aukin á. Markinu er ekki beitt á staka vöru á upprunalega listanum ef upprunamarkið fer yfir skilgreind mörk.</td>
<td>Eftirfarandi skýringarmynd sýnir snið. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>Eftirfarandi skýringarmynd sýnir gagnagjafana sem eru notaðir fyrir sniðið.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Eftirfarandi mynd sýnir niðurstöðuna þegar sniðið er keyrt. Í þessu tilviki er úttakið flatur listi yfir vörutegundir.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>Í eftirfarandi myndum hefur sama sniðið verið breytt þannig að það birtir listann yfir vörutegundir í runum þegar ein runa verður að innihalda vörutegundir og heildarþyngdin ætti ekki að fara yfir hámarkið 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Eftirfarandi mynd sýnir niðurstöðurnar þegar stillt snið er keyrt.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] Mark er ekki beitt á síðasta hlut í upprunalistanum, vegna þess að gildi (11) mörkum upprunans (þyngd) fer yfir skilgreind mörk (9). Notaðu annaðhvort <strong>WHERE</strong> aðgerðina eða <strong>Virkjað</strong> segðina á samsvarandi sniðseiningu til að hunsa (sleppa) undirlistum meðan á skýrslugerð stendur, eins og þurfa þykir.</blockquote>
</td>
</tr>
<tr>
<td>Afmörkun (listi, skilyrði)</td>
<td>Skila inn tilgreindan lista eftir að fyrirspurnin hefur verið breytt til að sía fyrir tilgreind skilyrði. Þessi aðgerð er frábrugðin <strong>WHERE</strong> aðgerðinni, vegna þess að tilgreint skilyrði er beitt á hvaða gagnagjafa rafrænnar skýrslugerðar af gerðinni <strong>Töflufærslur</strong> á gagnagrunnsstigi. Listinn og forsendurnar er hægt að skilgreina með því að nota töflur og samskipti.</td>
<td>Ef <strong>Lánardrottinn</strong> er stilltur sem gagnagjafi rafrænnar skýrslugerðar sem vísar til VendTable töflunnar, <strong>FILTER (Söluaðilar, Vendors.VendGroup = &quot;40&quot;)</strong> skilar aðeins lista yfir seljendur sem tilheyra söluhópi 40. Ef <strong>Lánardrottinn</strong> er stilltur sem gagnagjafi rafrænnar skýrslugerðar sem vísar til VendTable töflunnar og <strong>parmVendorBankGroup</strong> er stillt sem gagnagjafi rafrænnar skýrslugerðar sem skilar gildi af gagnagerðinni <strong>Strengur</strong> <strong>SÍA Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> skilar lista yfir bara lánardrottnalykla sem tilheyra ákveðnum bankaflokki.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Rökvirkni

| Aðgerð | lýsing | Dæmi |
|----------|-------------|---------|
| CASE (tjáning, valkostur 1, niðurstaða 1 \[, valkostur 2, niðurstaða 2\] … \[, sjálfgefin niðurstaða\]) | Meta tilgreind gildi segðar gagnvart tilgreindum öðrum valkostum. Skila niðurstöðu valmöguleikans sem jafngildir gildi segðarinnar. Annars skila valfrjálsu sjálfgefnu niðurstöðunni ef sjálfgefin niðurstaða er tilgreind. (Sjálfgefna niðurstaðan er síðasta breytan þar sem valmöguleiki kemur ekki á undan.) | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** skilar strengnum **"WINTER"** þegar núverandi setudagsetning Finance and Operations er á milli október og desember. Annars skilar það auður strengur. |
| IF (skilyrði, gildið 1, gildi 2) | Skila fyrsta tilgreinda gildið þegar tilgreinda skilyrðið er uppfyllt. Annars skila öðru tilgreinda gildina. Ef gildi 1 og gildi 2 eru færslur eða færslulistar, þá hefur niðurstaðan aðeins svæðina sem eru í báðum listunum. | **EF (1 = 2 "skilyrði er uppfyllt", "skilyrði er ekki í uppfyllt")** skilar strengurinn **"skilyrði er ekki uppfyllt"**. |
| NOT (ástand) | Skila öfugu röklega gildi tilgreinds skilyrðis. | **NOT (TRUE)** skilar **FALSE**. |
| AND (skilyrði 1\[, skilyrði 2, ...\]) | Skilar **TRUE** ef *öll* tilgreind skilyrði eru uppfyllt. Skila annars **FALSE**. | **AND (1=1, "a"="a")** skilar **TRUE**. **AND (1=2, "a"="a")** skilar **FALSE**. |
| OR (skilyrði 1\[, skilyrði 2, ...\]) | Skila **FALSE** ef *allar* tilgreind skilyrði eru röng. Skila **TRUE** ef *allar* tilgreind skilyrði eru sönn. | **OR (1=2, "a"="a")** skilar **TRUE**. |
| VALUEIN (innsláttur, listi, segð listaatriðis) | Ákveða hvort tilgreindur innsláttur passar við hvaða gildi hlutar sem er í tilgreindum lista. Skila **TRUE** ef tilgreindur innsláttur passar við niðurstöðurnar af því að keyra tilgreint tjáning fyrir að minnsta kosti eina færslu. Skila annars **FALSE**. Færibreyta **innsláttar** táknar slóð gagnaveitueiningar. Gildi þessarar einingar verður samsvarað. Færibreyta **listans** táknar slóð gagnaveitueiningar af gerðinni færslulisti sem listi yfir skrár sem innihalda tjáningu. Gildi þessarar einingar verður borið saman við tilgreindan innslátt. Tjáning **listaatriðis** táknar tjáningu sem annaðhvort bendir á eða inniheldur einn reit af tilgreindum lista sem á að nota við samsvörunina. | Til dæmis, sjá [dæmin: VALUEIN (innsláttur, listi, segð listaatriðis)](#examples-valuein-input-list-list-item-expression) í kaflanum sem fylgir. |

#### <a name="examples-valuein-input-list-list-item-expression"></a>Dæmi: VALUEIN (innsláttur, listi, segð listaatriðis)
Almennt er **VALUEIN** virknin þýdd yfir í sett af **OR** skilyrðum:

(inntak = list.item1.value) EÐA (innsláttur = list.item2.value) EÐA …

##### <a name="example-1"></a>Dæmi 1
Þú skilgreinir eftirfarandi gagnaveitu með vörpun líkansins: **Listi** (**Gerð reiknaðs** reits). Þessi gagnaveita inniheldur tjáninguna **SPLIT ("a,b,c", ",")**.

Þegar gagnaveita er kölluð sem er skilgreind sem **VALUEIN ("B", Listi, List.Value)** tjáning, skilar það **TRUE**. Í þessu tilviki er **VALUEIN** þýtt í eftirfarandi safn skilyrða:

**((„B“ = „a“) eða („B“ = „b“) eða („B“ = „c“))**, þar sem **(„B“ = „b“)** jafngildir **TRUE**

Þegar gagnaveita er kölluð sem er skilgreind sem **VALUEIN („B“, Listi, LEFT(List.Value, 0))** tjáning, skilar það **FALSE**. Í þessu tilviki er **VALUEIN** þýtt í eftirfarandi skilyrði:

**(„B“ = ““)**, sem er ekki jafnt **TRUE**

Athugaðu að efri mörkin fyrir fjölda stafa í texta slíks ástands eru 32.768 stafir. Þess vegna ættir þú ekki að búa til gagnaveitur sem kunna að fara yfir þessi mörk við keyrslu. Ef farið er yfir mörkin mun forritið stöðvast og undantekning kemur upp. Til dæmis getur þetta ástand komið fram ef gagnaveitan er skilgreind sem **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)** og listarnir **List1** og **List2** innihalda mikið magn af færslum.

Í sumum tilfellum er **VALUEIN** þýtt í gagnagrunnsstreng með því að nota **EXISTS JOIN** virknitáknið. Þessi hegðun kemur fram þegar **FILTER** virknin er notuð og eftirfarandi skilyrði eru uppfyllt:

- Slökkt er á valkostinum **ASK FOR QUERY** fyrir gagnaveitu **VALUEIN** aðgerðarinnar sem vísar til listann yfir skrár. (Engar viðbótarskilyrði verða beittar á þessum gagnaveitum meðan á keyrslu stendur.)
- Engar faldaðar tjáningar eru stilltar fyrir gagnaveituna **VALUEIN** aðgerðina sem vísar til listans yfir skrár.
- Listaatriði **VALUEIN** aðgerðarinnar vísar til reitar (ekki tjáningu eða aðferðar) af tilgreindri gagnaveitu.

Íhugaðu að nota þennan valkost í staðinn fyrir **WHERE** aðgerðina eins og lýst er hér að framan í þessu dæmi.

##### <a name="example-2"></a>Dæmi 2

Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:

- **IN** (**Gerðin** töflufærslur), sem vísar til Intrastat töflunni
- **Port** (**Gerðin** töflufærslur), sem vísar til IntrastatPort töflunni

Þegar gagnaveita er kölluð sem er stillt sem **FILTER (IN, VALUEIN (In.Port, Port, Port.PortId)** tjáningu, er eftirfarandi SQL-skipun sköpuð til að skila síuðum færslum af Intrastat töflunni:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Fyrir **dataAreaId** reiti er endanleg SQL-skipun mynduð með því að nota **IN** virknitákn.

##### <a name="example-3"></a>Dæmi 3

Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:

- **Le** (**Gerð reiknaðs** reits), sem inniheldur tjáningu **SPLIT (“DEMF, GBSI, USMF“, “,“)**
- **IN** (**Gerðin** töflufærslur), sem vísar til Intrastat töflunni og þar sem **Á milli fyrirtækja** valkosturinn er kveiktur á

Þegar gagnaveita er kölluð sem er stillt sem **FILTER (IN, VALUEIN (In.dataAreaId, Le, Le.Value)** tjáning, inniheldur endanleg SQL-skipun eftirfarandi skilyrði:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>Reikniaðgerðir

| Aðgerð | lýsing | Dæmi |
|----------|-------------|---------|
| ABS (númer) | Skila algildu gildi á tilgreindu tölunni. (Með öðrum orðum skal skila tölunni án táknsins.) | **ABS (-1)** skilar **1**. |
| POWER (númer, valdheimild) | Skilan niðurstöðum af því að hækka tilgreinda jákvæða tölu upp að tilgreindri valdheimild. | **POWER (10, 2)** skilar **100**. |
| NUMBERVALUE (streng aukastaf, skiltákn stafaflokkunar) | Umbreyta strengnum í númer. Tilgreint tugabrot er notað á milli heiltala og aukastafa fyrir tölu í tugakerfinu. Tilgreint skiltákn talna er notað til að skipta niður í þúsundasta hluta. | **NUMBERVALUE("1 234,56", ",", " ")** skilar gildinu **1234.56**. |
| VALUE (strengur) | Umbreyta strengnum í númer. Kommur og punktar (.) skoðast sem skiltákn aukastafa, og bandstrik fremst (-) er notað sem neikvætt formerki. Beita undantekningu ef tilgreindur strengur inniheldur önnur tákn sem eru ekki tölur. | **VALUE ("1 234,56")** beitir undantekningu. |
| ROUND (númer, aukastafir) | Skila tilgreindri tölu eftir að hún hefur verið námunduð að tilgreindum fjölda aukastafa:<ul><li>Ef gildi **aukastafanna** er meira en 0 (núll), er tilgreind tala námunduð að þetta mörgum aukastöfum.</li><li>Ef gildi **aukastafa** er **0** (núll), er tilgreind tala námunduð að næstu heiltölu.</li><li>Ef gildi **aukastafa** er minna en 0 (núll), er tilgreind tala námunduð til vinstri við tugastafinn.</li></ul> | **ROUND (1200.767, 2)** sléttar tvo aukastafi og skilar **1200.77**. **ROUND (1200.767, -3)** sléttar næsta margfeldi svæðisins 1.000 og skilar **1000**. |
| ROUNDDOWN (númer, aukastafir) | Skila tilgreindri tölu eftir að hún hefur verið námunduð niður í tilgreindan fjölda aukastafa.<blockquote>[!NOTE] Þessi aðgerð hegðar sér eins og **ROUND**, en hún námundar alltaf tilgreindri tölu niður (í átt að núlli).</blockquote> | **ROUNDDOWN (1200.767, 2)** sléttar niður á við tvo aukastafi og skilar **1200.76**. **ROUNDDOWN (1700.767, -3)** sléttar niður á við næsta margfeldi svæðisins 1.000 og skilar **1000**. |
| ROUNDUP (númer, aukastafir) | Skila tilgreindri tölu eftir að hún hefur verið námunduð upp í tilgreindan fjölda aukastafa.<blockquote>[!NOTE] Þessi aðgerð hegðar sér eins og **ROUND**, en hún námundar tilgreindri tölu upp (í átt frá núlli).</blockquote> | **ROUNDUP (1200.763, 2)** sléttar upp að tvo aukastafi og skilar **1200.77**. **ROUNDUP (1200.767, -3)** sléttar upp að næsta margfeldi svæðisins 1.000 og skilar **2000**. |

### <a name="data-conversion-functions"></a>Gagnaumbreytingarvirkni

| Aðgerð | lýsing | Dæmi |
|----------|-------------|---------|
| VALUE (strengur) | Umbreyta strengnum í númer. Kommur og punktar (.) skoðast sem skiltákn aukastafa, og bandstrik fremst (-) er notað sem neikvætt formerki. Beita undantekningu ef tilgreindur strengur inniheldur önnur tákn sem eru ekki tölur. | **VALUE ("1 234,56")** beitir undantekningu. |
| NUMBERVALUE (streng aukastaf, skiltákn stafaflokkunar) | Umbreyta strengnum í númer. Tilgreint tugabrot er notað á milli heiltala og aukastafa fyrir tölu í tugakerfinu. Tilgreint skiltákn talna er notað til að skipta niður í þúsundasta hluta. | **NUMBERVALUE("1 234,56", ",", "")** skilar **1.234,56**. |
| INTVALUE (strengur) | Skila heiltölu framsetningu á tiltgreindum streng. Allir aukastafir eru styttir. | **INTVALUE ("100.77")** skilar **100**. |
| INTVALUE (fjöldi) | Skila heiltölu framsetningu á tilgreindri tölu. Allir aukastafir eru styttir. | **INTVALUE (-100.77)** skilar **-100**. |
| INT64VALUE (strengur) | Skila int64 framsetning á tilgreindum streng. Allir aukastafir eru styttir. | **INT64VALUE ("22565422744")** skilar **22565422744**. |
| INT64VALUE (númer) | Skila int64 framsetningu á tilgreindri tölu. Allir aukastafir eru styttir. | **INT64VALUE (22565422744.00)** skilar **22565422744**. |

### <a name="record-functions"></a>Færsluvirkni

| Aðgerð | lýsing | Dæmi |
|----------|-------------|---------|
| NULLCONTAINER (listi) | Skila **núll** færslu sem hefur sömu skipan og tilgreind færsluskrár eða færsla.<blockquote>[!NOTE] Þessi aðgerð er úrelt. Notið **EMPTYRECORD** í staðinn.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** skilar nýja tóma skráningu sem hefur sömu skipan sem listanum sem var skilað af **SPLIT** aðgerð. |
| EMPTYRECORD (skráning) | Skila **núll** færslu sem hefur sömu skipan og tilgreind færsluskrár eða færsla.<blockquote>[!NOTE] Færsla **núll** er færsla þar sem allir reitir eru með tómt gildi. Tómt gildi er **0** (núll) fyrir tölur, tóman streng fyrir strengi og svo framvegis.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** skilar nýja tóma lista sem hefur sömu skipan sem listanum sem var skilað af **SPLIT** aðgerð. |

### <a name="text-functions"></a>Textavirkni

<table>
<thead>
<tr>
<th>Aðgerð</th>
<th>lýsing</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (strengur)</td>
<td>Skila tilgreindum streng eftir að honum hefur verið breytt í hástafi.</td>
<td><strong>UPPER(&quot;Dæmi&quot;)</strong> skilar <strong>&quot;DÆMI&quot;</strong>.</td>
</tr>
<tr>
<td>LOWER (strengur)</td>
<td>Skila tilgreindum streng eftir að honum hefur verið breytt í lágstafir.</td>
<td><strong>LOWER (&quot;Dæmi&quot;)</strong> skilar <strong>&quot;dæmi&quot;</strong>.</td>
</tr>
<tr>
<td>LEFT (streng, fjölda stafa)</td>
<td>Skilar tilteknum fjölda stafa úr upphafi tiltekins strengs.</td>
<td><strong>LEFT (&quot;Dæmi&quot;, 3)</strong> skilar <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr>
<td>RIGHT (streng, fjölda stafa)</td>
<td>Skilar tilteknum fjölda stafa úr enda tiltekins strengs.</td>
<td><strong>RIGHT (&quot;Dæmi&quot;, 3)</strong> skilar <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr>
<td>MID (streng, byrjunarstöðu, fjölda stafa )</td>
<td>Skilar tilteknum fjölda stafa úr enda tiltekins strengs, og byrjar í tiltekinni stöðu.</td>
<td><strong>MID (&quot;Dæmi&quot;, 2, 3)</strong> skilar <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr>
<td>LEN (strengur)</td>
<td>Skilar fjölda stafa í tilteknum streng..</td>
<td><strong>LEN (&quot;Dæmi&quot;)</strong> skilar <strong>6</strong>.</td>
</tr>
<tr>
<td>CHAR (númer)</td>
<td>Skila streng af stöfum sem vísað er til með tilgreinda Unicode númerinu.</td>
<td><strong>CHAR (255)</strong> skilar <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE] Strengurinn sem þessi aðgerð skilar veltur á kóðuninni sem er valin í yfireiningu FILE sniðsins. Fyrir listann yfir studdar kóðanir, sjá <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kóðunarflokkur</a>.</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (string 1 [, string 2, …])</td>
<td>Skila öllum tilgreindum textastrengjum eftir að þeir hafa verið tengdir í eina streng.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> skilar <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE] Segðin <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> skilar einnig <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (strengur mynstur, útskipting)</td>
<td>Skila tilgreindum streng eftir að öll tilfelli stafa í tilgreindum mynsturstreng hafa verið skipt út fyrir stafina í samsvarandi stöðu í tilgreindum skiptistreng.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> kemur í stað mynstursins <strong>&quot;cd&quot;</strong> með strengur <strong>&quot;GH&quot;</strong> og skilar <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>REPLACE (streng, mynstur, útskipting, er flagg fyrir reglulega segð)</td>
<td>Þegar tilgreind færibreyta <strong>flaggs fyrir reglulega segð</strong> er <strong>sönn</strong>, skilaðu reglulegri segð eftir að honum hefur verið breytt með því að beita reglulegu segðinni sem er tilgreind sem <strong>mynstur</strong> frumbreytu fyrir þessa aðgerð. Þessi segð er notuð til að finna stafi sem verður að skipta út. Stafir tilgreindrar <strong>staðgengilsbreytu</strong> eru notaðar til að skipta út stöfum sem finnast. Þegar tilgreind færibreyta <strong>flaggs fyrir reglulega segð</strong> er <strong>ósönn</strong>, virkar þessi aðgerð eins og <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> notar reglulega segð sem fjarlægja öll tákn sem ekki eru tölur og skilar <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> kemur í stað mynsturs <strong>&quot;cd&quot;</strong> með strengur <strong>&quot;GH&quot;</strong> og skilar <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>TEXT (inntak)</td>
<td>Skila tilgreindu inntaki eftir að því hefur verið breytt í textastreng sem er sniðið í samræmi við stillingar á þjónsstaðsetningu á núverandi tilviki Finance and Operations. Fyrir gildi í af gerðinni <strong>rauntala</strong> takmarkast umbreyting strengs við sem nemur tveimur tugasætum.</td>
<td>Ef þjónsstaðsetning á tilviki Finance and Operations er skilgreind sem <strong>EN-US</strong>, <strong>TEXTI (nú ())</strong> skilar núverandi setudagsetningu Finance and Operations, desember 17, 2015, sem textastrenginn <strong>&quot;12/17/2015 07:59:23 fyrir hádegi&quot;</strong>. <strong>TEXT (1/3)</strong> skilar <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr>
<td>FORMAT (strengur 1, strengur 2[, strengur 3, ...])</td>
<td>Skila tilgreindum streng eftir að hann hefur verið sniðinn með því að skipta öllum tilvikum af <strong>%N</strong> með <em>n</em> frumbreytunni. Frumbreytur eru strengir. Ef frumbreyta er ekki gefin upp fyrir færibreytu, er færibreytan skilað sem <strong>&quot;%N&quot;</strong> í strengnum. Fyrir gildi í af gerðinni <strong>rauntala</strong> takmarkast umreikningur strengs við sem nemur tveimur tugasætum.</td>
<td>Í eftirtöldum myndum skilar <strong>PaymentModel</strong> gagnagjafinn færslulista viðskiptavina með þætti <strong>viðskiptavini</strong> og gildi vinnsludagsetningar með <strong>ProcessingDate</strong> svæðið.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>Í sniði rafrænnar skýrslugerðar (ER) sem er hannað til að mynda rafræna skrá fyrir valda viðskiptavini <strong>PaymentModel</strong> er valinn sem gagnagjafa og stýrir flæði ferlis. Beitt er undantekningu til að upplýsa notandann þegar valinn viðskiptavinur er hættur á deginum sem skýrslan er unnin. Formúlu sem er hannað fyrir þessa gerð vinnslustýringar getur notað eftirfarandi tilföng:</p>
<ul>
<li>Finance and Operations merki SYS70894 sem hefur eftirfarandi texta:
<ul>
<li><strong>Fyrir tungumál EN-US:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Fyrir tungumálið DE:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Finance and Operations merki SYS18389 sem hefur eftirfarandi texta:
<ul>
<li><strong>Fyrir tungumál EN-US:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>Fyrir tungumál DE:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Hér er formúlunnar sem hægt er að hanna:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Ef skýrsla er unnin fyrir <strong>Litware Retail</strong> viðskiptavin 17. desember 2015, í <strong>EN-US</strong> menningu og <strong>EN-US</strong> tungumáli, skilar þessi formúla eftirfarandi texta, sem hægt er að birta fyrir notandann sem undantekningarskilaboð:</p>
<p>&quot;Ekkert til að prenta. Viðskiptavinur Litware Smásölu er lokaður fyrir 17/12/2015.&quot;</p>
<p>Ef sama skýrslan er unnin fyrir viðskiptavininn <strong>Litware Retail</strong> þann 17. desember 2015 í menningunni <strong>DE</strong> og tungumálinu <strong>DE</strong> skilar formúlan eftirfarandi texta, sem notar annað snið dagsetningar:</p>
<p>&quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE] Eftirfarandi setningafræði er beitt í formúlum rafrænnar skýrslugerðar fyrir merki:
<ul>
<li><strong>Fyrir merki úr tilföngum Finance and Operations:</strong> <strong>@&quot;X&quot;</strong>, þar sem <strong>X</strong> merkjakennið í hugbúnaðarhlutatrénu (AOT)</li>
<li><strong>Fyrir merki sem eru í skilgreiningum rafrænnar skýrslugerðar:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, þar sem <strong>X</strong> er merkjakenni í skilgreiningu rafrænnar skýrslugerðar</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (númer, snið)</td>
<td>Skila streng með framsetningu tiltekinnar tölu í tilgreindu sniði. (Fyrir upplýsingar um studd snið sjá <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">staðlað</a> og <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">sérsniðna</a>.) Samhengi sem þessi aðgerð er keyrð í ákvarðar þá menningu sem er notuð til að sníða vörunúmer.</td>
<td>Fyrir EN-US menningu, <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> skilar <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> skilar <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (númer, tungumál, gjaldmiðil, prenta flaggheiti gjaldmiðils, tugakomma)</td>
<td>Skila inn tilgreindri tölu eftir að hún hefur verið stafsett (breytt í textastreng) á tilgreint tungumál. Tungumálakóðinn er valfrjáls. Þegar hann er skilgreindur sem tómur strengur er tungumálakóðinn fyrir samhengið sem er í keyrslu notaður. (Tungumálakóðinn fyrir samhengið sem er keyrt er skilgreint fyrir myndaða möppu eða skrá.) Tungumálakóðinn er einnig valfrjáls. Þegar hann er skilgreindur sem tómur strengur, er gjaldmiðill fyrirtækis notaður.
<blockquote>[!NOTE] <strong>Prentun gjaldeyrisheitis</strong> og breytur <strong>aukastafa</strong> eru greindar aðeins fyrir eftirfarandi tungumálakóða: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> og <strong>RU</strong>. Þar að auki er breytan fyrir <strong>prentun gjaldeyrisheitis</strong> aðeins greind fyrir Finance and Operations fyrirtæki þar sem samhengi landsins eða svæðisins styður frávik frá gjaldmiðlaheiti.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> Skilar <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot; false, 0)</strong> skilar <strong>&quot;“Sto dwadzieścia”&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> skilar <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr>
<td>PADLEFT (strengur, lengd, stafir til fyllingar)</td>
<td>Skila streng af tilgreindri lengd, þar sem upphaf tilgreinds strengs er fyllt með tilgreindum stöfum.</td>
<td><strong>PADLEFT (&quot;“1234”&quot;, 10, &quot;&nbsp;&quot;)</strong> skilar textastreng <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“1234”&quot;</strong>.</td>
</tr>
<tr>
<td>TRIM (strengur)</td>
<td>Skila tilgreindum textastreng eftir að bilum fyrir framan og aftan hefur verið eytt, og eftir að samfelld bil milli orðanna hafa verið fjarlægð.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dæmi&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;texta&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> skilar <strong>&quot;sýnishornatexta&quot;</strong>.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (slóð tölusetningargagnagjafa, merkjatexti tölusetningargildis)</td>
<td>Skila gildi á tilgreindum tölusetningum gagnagjafa, byggt á tilgreindum texta tölusetningarmerkis.</td>
<td>Í eftirfarandi mynd er <strong>ReportDirection</strong> upptalningin kynnt í gagnalíkani. Athugaðu að merki eru skilgreind fyrir tölusetningargildi.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Eftirfarandi mynd sýnir þessar upplýsingar:</p>
<ul>
<li><strong>ReportDirection</strong> tölusetningarlíkanið er sett í skýrslu sem gagnagjafi, <strong>$ Direction</strong>.</li>
<li>Segð rafrænnar skýrslugerðar, <strong>$ IsArrivals</strong>, er hönnuð til að nota tölusetningarlíkanið sem breytu af þessari aðgerð. Gildi þessarar segðar er <strong>TRUE</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (inntak)</td>
<td>Umbreyta tilgreindu inntaki af gagnagerðinni <strong>Strengur</strong> í gagnaatriði af gagngerðinni <strong>GUID</strong>.<blockquote>[!NOTE] Til að umbreyta í gagnstæða átt (það er að breyta tilteknu inntaki <strong>GUID</strong> gagnagerðarinnar í gagnaatriði <strong>Strengur</strong> gagnagerðarinnar) er hægt að nota <strong>TEXT ()</strong> virknina.</blockquote></td>
<td>Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:
<ul>
<li><strong>myID</strong> (gerðin <strong>Reiknaður reitur</strong>) sem inniheldur segðina <strong>GUIDVALUE (&quot;AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0&quot;)</strong></li>
<li><strong>Notendur</strong> (gerðin <strong>Töflufærslur</strong>) sem vísar til töflunnar UserInfo</li>
</ul>
Þegar þessir gagnagjafar eru skilgreindir er hægt að nota segð eins og <strong>SÍA (Users, Users.objectId = myID)</strong> til að sía UserInfo töfluna með reitnum <strong>objectId</strong> af gagnagerðinni <strong>GUID</strong>.
</td>
</tr>
<tr>
<td>JSONVALUE (auðkenni, slóð)</td>
<td>Þátta gögn í JavaScript Object Notation (JSON) sniði sem er aðgengilegt með tilgreindri slóð til að draga út tölugildi sem byggist á tilgreindu auðkenni.</td>
<td>Gagnagjafinn <strong>$JsonField</strong> inniheldur eftirfarandi gögn í JSON sniði: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. Fyrir þennan gagnagjafa skilar </strong>JSONVALUE (&quot;BuildNumber&quot;, $JsonField)</strong> gildinu <strong>7.3.1234.1</strong> af gagngerðinni <strong>Strengur</strong>.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Gagnaumbreytingarvirkni

| Aðgerð | lýsing | Dæmi |
|----------|-------------|---------|
| TEXT (inntak) | Skila tilgreindu inntaki eftir að því hefur verið breytt í textastreng sem er sniðið í samræmi við stillingar á þjónsstaðsetningu á núverandi tilviki Finance and Operations. Fyrir gildi í af gerðinni **real** ,umreikning strengs takmarkast við sem nemur tveimur tugasætum. | Ef þjónsstaðsetning á tilviki Finance and Operations er skilgreind sem **EN-US**, **TEXTI (nú ())** skilar núverandi setudagsetningu Finance and Operations, desember 17, 2015, sem textastrenginn **12/17/2015 07:59:23 fyrir hádegi**. **TEXT (1/3)** skilar **"0.33"**. |
| QRCODE (strengur) | Skila mynd QR-kóða (Quick Response Code) í base64 tvíundarsniði fyrir tilgreindan streng. | **QRCODE ("Sample Text")** skilar **U2FtcGxlIHRleHQ =**. |

### <a name="data-collection-functions"></a>Gagnasöfnunaraðgerðir

| Aðgerð | lýsing | Dæmi |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Skila heiti á núverandi einingu sniðs. Skila tómum streng þegar slökkt er á **Safnaðu úttaks upplýsingar** flaggi núverandi skráa. | Til að læra meira um hvernig á að nota þessa aðgerð, sjáðu **Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman** leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli. |
| SUMIFS (lykilstrengur fyrir samlagningu, skilyrði svið1, skilyrði gildi1 strengur \[, skilyrði svið2 strengur skilyrði gildi2 strengur, …\]) | Skila summu gilda sem safnað var fyrir XML-hnúta (þar sem heitið er skilgreint sem lykill) þegar sniðið var keyrt og sem uppfyllir tilgreind skilyrði (pör af sviðum og gildum). Skila **0** (núll) gildi þegar slökkt er á **Safna upplýsingum úttaks** flaggi núverandi skráar. | |
| SUMIF (lykilstreng fyrir samlagningu strengur, strengur skilyrðasviðs, strengur skilyrðagilda...]) | Skila summu gilda sem safnað var fyrir XML-hnúta (þar sem heitið er skilgreint sem lykill) þegar sniðið var keyrt og sem uppfyllir tilgreind skilyrði (svið og gildi). Skila **0** (núll) gildi þegar slökkt er á **Safna upplýsingum úttaks** flaggi núverandi skráar. | |
| COUNTIFS (skilyrði svið1 strengur, skilyrði gildi1 strengur \[, skilyrði svið2 strengur, skilyrði gildi2 strengur, …\]) | Skila fjölda XML-hnúta sem safnað var þegar sniðið var keyrt og það uppfyllir tilgreind skilyrði (pör af sviðum og gildum). Skila **0** (núll) gildi þegar slökkt er á **Safna upplýsingum úttaks** flaggi núverandi skráar. | |
| COUNTIF (strengur skilyrðasviðs, strengur skilyrðagildis) | Skila fjölda XML-hnúta sem var safnað þegar sniðið var keyrt og það uppfyllir tilgreint ástand (svið og gildi). Skila **0** (núll) gildi flaggsins þegar slökk er á **Safna upplýsingum úttaks** flaggi núverandi skráa. | |
| COLLECTEDLIST (skilyrði svið1 strengur, skilyrði gildi1 strengur \[, skilyrði svið2 strengur, skilyrði gildi2 strengur, …\]) | Skila lista yfir gildi sem var safnað fyrir XML-hnúta þegar sniðið var keyrt og það uppfyllir tilgreind skilyrði (svið og gildi). Skila tómum lista þegar slökkt er á **Safna upplýsingum úttaks** flaggi núverandi skráa. | |

### <a name="other-business-domainspecific-functions"></a>Other (lénsértæk virkni fyrir viðskipti)

| Aðgerð | lýsing | Dæmi |
|----------|-------------|---------|
| CONVERTCURRENCY (upphæð, frumgjaldmiðils, mark gjaldmiðil, dagsetning, fyrirtækisins) | Umreikna tilgreinda peningaupphæð frá tilgreindum upprunagjaldmiðli til tilgreinds markgjaldmiðils með því að nota stillingar tilgreinds Finance and Operations fyrirtækis á tilteknum degi. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** skilar jafngildi einni evru í Bandarískum dollurum á dagsetningu núverandi setu, byggða á stillingum DEMF-fyrirtækisins. |
| ROUNDAMOUNT (tölu, aukastafi, sléttunarreglu) | Námunda tilgreinda upphæð í tilgreindan fjölda aukastafa í samræmi við tilgreinda námundunarreglu.<blockquote>[!NOTE] Námundunarreglan verður að vera skilgreind sem tölusetningargildi **RoundOffType** Finance and Operations.</blockquote> | Ef **model.RoundOff** færibreyta er stillt á **Niður**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** skilar gildinu **1000,78**. Ef **model.RoundOff** færibreyta er stillt á annað hvort **Venjuleg** eða **Sléttun**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** skilar gildinu **1000.79**. |
| CURCredRef (tölur) | Skila Tilvísun lánardrottins, byggt á tölustöfum í tilgreint reikningsnúmeri. | **CURCredRef ("VEND-200002")** skilar **"2200002"**. |
| MOD\_97 (tölustafir) | Skila Tilvísun lánardrottins, sem MOD97 segð, byggt á tölustöfum tilgreinds reikningsnúmers. | **MOD\_97 ("VEND-200002")** skilar **"20000285"**. |
| ISOCredRef  (tölur) | Skila tilvísun alþjóðaviðskiptastofnunar um staðla (ISO), byggt á tölustöfum og stafrófstáknum í tilgreindu númeri vörureiknings.<blockquote>[!NOTE] Til að útiloka tákn frá stafrófum sem ekki eru í samræmi við ISO skal inntakshbreytan þýdd áður en hún er sett inn í þessa aðgerð.</blockquote> | **ISOCredRef ("VEND-200002")** skilar **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (strengur, númer) | Sækja tilgreint fjárhagslegt viðbótarvíddarkenni. Í færibreytunni **strengur** eru víddir táknaðar sem auðkenni sem eru aðskilin með kommum. Færibreytan **númer** skilgreinir kóða númeraraðar af umbeðinni vídd í strengnum. | **CN\_GBT\_AdditionalDimensionID ("AA, BB, CC, DD, EE, FF, GG, HH", 3)** skilar **"CC"**. |
| GetCurrentCompany () | Skila textaframsetningu á kóðanum fyrir lögaðilann (fyrirtæki) sem notandi er skráður inn á. | **GETCURRENTCOMPANY ()** skilar **USMF** fyrir notanda sem er skráður inn á **Contoso Entertainment System USA** fyrirtæki í Finance and Operations. |
| CH\_BANK\_MOD\_10 (tölustafir) | Skila tilvísun kröfuhafa sem MOD10 segð, byggt á tölum á tilgreindu númeri vörureiknings. | **CH\_BANK\_MOD\_10 ("VEND-200002")** skilar **3**. |
| FA\_SUM (kóði eignar, kóði virðislíkans, upphafsdagsetning, lokadagsetning) | Skila tilbúnum gagnageymi með stöðu eignar fyrir tilgreint tímabil. | **FA\_SUM (""COMP-000001", "Current", Date1, Date2)** skilar tilbúnum gagnageymi eignarinnar **"COMP-000001"** sem hefur **"Núverandi“** gildislíkan fyrir tímabil frá **Date1** til **Date2**. |
| FA\_BALANCE (kóði eignar, kóði virðislíkans, skýrslugjafarár, reikningsskiladagur) | Skila tilbúnum gagnageymi með stöðu eignar. Uppgjörsárið verður að vera tilgreint sem tölusetningargildi á **AssetYear** í Finance and Operations. | **FA\_SUM ("COMP-000001", "Núverandi", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** skilar tilbúnum gagnageymi fyrir stöðu eignar **"COMP-000001"** sem hefur **"Núverandi"** gildislíkan á núverandi setudagsetningu Finance and Operations. |
| TABLENAME2ID (strengur) | Skila heiltöluframsetningu af töfluauðkenni fyrir tilgreint töfluheiti. | **TABLENAME2ID ("Intrastat")** skilar **1510**. |
| ISVALIDCHARACTERISO7064 (strengur) | Skila Boolean gildi **TRUE** þegar tilgreindur strengur táknar gildan alþjóðlegan bankareikning (IBAN). Annars skila Boolean gildi **FALSE**. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** skilar **SATT**. **ISVALIDCHARACTERISO7064 ("AT61")** skilar **RANGT**. |
| NUMSEQVALUE (númeraraðarkóði, umfang, umfangskenni) | Skila nýmynduðu gildi númeraraðar, byggt á tilgreindum númeraraðarkóða, umfangi og umfangskenni. Umfangið verður að tilgreina sem gildi **ERExpressionNumberSequenceScopeType** tölusetningarinnar (**Samnýtt**, **Lögaðili** eða **Fyrirtæki**). Fyrir **Samnýtt**, tilgreindu tóman streng sem umfangskenni. Fyrir umfang **Fyrirtækis** og **Lögaðila**, tilgreindu fyrirtækjakóðann og umfangskennið. Fyrir umfang **Fyrirtækis** og **Lögaðila**, ef tilgreindur er tómur strengur sem umfangskennið, er núverandi fyrirtækjakóði notaður. | Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:<ul><li>**enumScope** (**Dynamics 365 for Operations gerð** tölusetningar), sem vísar til **ERExpressionNumberSequenceScopeType** tölusetningarinnar</li><li>**NumSeq** (**Gerðin reiknaður** reitur), sem inniheldur tjáningu **NUMSEQVALUE („Gene\_1“, enumScope.Company, ““)**</li></ul>Þegar **NumSeq** gagnaveitan er kölluð skilar hún nýmynduðu gildi **Gene\_1** númeraröðarinnar sem hefur verið skilgreint fyrir fyrirtækið sem leggur til samhengið sem ER-sniði er keyrt undir. |
| NUMSEQVALUE (númeraraðarkóði) | Skila nýmynduðu gildi númeraraðar, byggt á tilgreindu númeraröðinni, umfangi **Fyrirtæki**, og (sem umfangskenni) kóði fyrirtækisins sem leggur til samhengið sem er ER-snið er keyrt undir. | Þú skilgreinir eftirfarandi gagnaveitu með vörpun líkansins: **NumSeq** (**Gerð reiknaðs** reits). Þessi gagnaveita inniheldur tjáninguna **NUMSEQVALUE („Gene\_1“)**. Þegar **NumSeq** gagnaveitan er kölluð skilar hún nýmynduðu gildi **Gene\_1** númeraröðarinnar sem hefur verið skilgreint fyrir fyrirtækið sem leggur til samhengið sem ER-sniði er keyrt undir. |
| NUMSEQVALUE (færslukenni númeraraðar) | Skila nýmynduðu gildi númeraraðar, byggt á tilgreindu færslukenni númeraraðar. | Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:<ul><li>**LedgerParms** (**Gerð** töflu), sem vísar til LedgerParameters töflunnar</li><li>**NumSeq** (**Gerð reiknaðs** reits), sem inniheldur tjáninguna **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)**</li></ul>Þegar **NumSeq** gagnaveitan er kölluð skilar hún nýmynduðu gildi númeraraðarinnar sem hefur verið skilgreint í fjárhagsfæribreytum fyrir fyrirtækið sem leggur til samhengið sem ER-sniði er keyrt undir. Þessi númeraröð auðkennir færslubókina á einkvæman hátt og vinnur sem lotunúmer sem tengir færslurnar saman. |

### <a name="functions-list-extension"></a>Viðbót við lista yfir virkni

Rafræn skýrslugerð styður möguleikann á að útvíkka listann yfir aðgerðir sem eru notaðar í segðir rafrænnar skýrslugerðar. Þetta krefst smá verkfræðikunnáttu. Fyrir ítarlegar upplýsingar sjá [Útvíkka listann fyrir aðgerðir rafrænnar skýrslugerðar](general-electronic-reporting-formulas-list-extension.md)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Útvíkka listann yfir aðgerðir Rafrænnar skýrslugerðar](general-electronic-reporting-formulas-list-extension.md)

