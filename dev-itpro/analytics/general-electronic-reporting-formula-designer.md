---
title: "Formúluhönnuður í Rafræna Skýrslugerð"
description: "Þessi Umfjöllunarefni útskýrir hvernig nota á formúluhönnuður í Rafræna skýrslugerð (ER). Þegar hönnuð er snið fyrir ákveðna rafrænna skjala í rafrænni skýrslugerð geturðu notað Microsoft Excel – eins og formúlur fyrir umbreytingu gagna til að uppfylla þarfir fyrir uppfyllingu skjals sem og snið. Ýmsar gerðir aðgerða eru studd - texta, dagsetningu og tíma, stærðfræðilega röklegt, upplýsingar um gerð gagnaumbreyting og aðrar (business lén – sérstakar aðgerðir)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ac8d6c064ca826cc1c2fed07578ca9ce0c66ef66
ms.lasthandoff: 03/31/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Formúluhönnuður í Rafræna Skýrslugerð

Þessi Umfjöllunarefni útskýrir hvernig nota á formúluhönnuður í Rafræna skýrslugerð (ER). Þegar hönnuð er snið fyrir ákveðna rafrænna skjala í rafrænni skýrslugerð geturðu notað Microsoft Excel – eins og formúlur fyrir umbreytingu gagna til að uppfylla þarfir fyrir uppfyllingu skjals sem og snið. Ýmsar gerðir aðgerða eru studd - texta, dagsetningu og tíma, stærðfræðilega röklegt, upplýsingar um gerð gagnaumbreyting og aðrar (business lén – sérstakar aðgerðir).

<a name="formula-designer-overview"></a>Yfirlit Formúluhönnuður.
-------------------------

Formúluhönnuður sem styður rafræn skýrslugerð (ER). Þess vegna á hönnunartíma er hægt að skilgreina segðir sem nota má fyrir eftirfarandi verk í keyrslutíma:

-   Umbreytingu gagna úr Microsoft Dynamics 365 for Operations gagnagrunninum sem eiga að vera fyllt út í gagnalíkan rafrænnar skýslugerðar sem er hannað til að gagnagjafa fyrir skrársniðmát rafrænnar skýrslugerðar (síun, flokkun, gerðir gagnaumbreytinga o.s.frv.)
-   Sníðing gagna sem verður að senda í myndandi rafræna skjalið í samræmi við útlit og skilyrði fyrir tiltekna snið rafrænnar skýrslugerðar (í samræmi við umbeðna tungumálið eða menning, dulritun o.s.frv.)
-   Stýrir ferli fyrir myndun rafrænna skjala (virkjun / óvirkja úttak tiltekinna eininga sniðs, háð vinnslugögn, trufla myndun skjala, senda skilaboð til endanotenda, o.s.frv.)

Hægt að opna síðu formúluhönnuðar ef þú gerir eitt af eftirfarandi:

-   Bindingu gagnaveituvöru við þætti gagnalíkans.
-   Bindingu gagnaveituvöru við þætti til að sníða.
-   Fullt Viðhald á reiknuðum svæðum sem hluta af gagnagjafa
-   Skilgreining sýnileikaskilyrða fyrir innsláttarfæribreytur notanda
-   Hönnun á umbreytingum sniðsins
-   Skilgreining á virkjun skilyrða fyrir þætti sniðsins.
-   Skilgreining á skrárheiti fyrir FILE-þætti sniðsins.
-   Skilgreining á skilyrðum fyrir villuleit ferlisstýringar.
-   Skilgreining á texta í skilaboðum fyrir villuleit á ferlisstýringu.

## <a name="designing-er-formulas"></a>Hönnun á formúlum fyrir rafræna skýrslugerð
### <a name="data-binding"></a>gagnatengsl

Formúluhönnuð ER má nota til að skilgreina segðir sem umbreytir gögnum sem er tekið úr gagnagjafa, þannig að hægt sé að nota gögnin til að fylla inn í gagnanotanda á keyrslutíma.

-   Úr Dynamics 365 for Operations gagnagjafa og færibreytur keyrslutíma til gagnalíkans rafrænnar skýrslugerðar.
-   Úr gagnalíkani rafrænnar skýrslugerðar yfir í snið rafrænnar skýrslugerðar.
-   Úr Dynamics 365 for Operations gagnagjafa og færibreytur keyrslutíma til sniðs rafrænnar skýrslugerðar.

Eftirfarandi skýringarmynd sýnir hönnun segðar af þessari gerð. Í þessu dæmi skilar segðin gildinu **Intrastat.AmountMST** á svæði Dynamics 365 for Operations **Intrastat** töflu, eftir gildið var sléttað sem nemur tveimur tugasætum. [![mynd segð bindingu](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) eftirfarandi dæmi sýnir hvernig hægt er að nota segð sem samanstendur af þessari gerð. Í þessu dæmi er niðurstaða designed segð er fyllt út í í **Transaction.InvoicedAmount** þátt í **vsk-skýrslugerð líkan** gagnalíkan. [![mynd segð binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) í keyrslutíma, designed formúlu **fjárhagsvídd SLÉTTUNARTAPS (Intrastat.AmountMST, 2)**, verður að slétta í virðis á **AmountMST** fyrir hverja færslu af á **Intrastat** töfluna tvo aukastafi og sléttuðum gildi til að fylla út í **Transaction.InvoicedAmount** hluti á **-skýrslugerð** gagnalíkan.

### <a name="data-formatting"></a>Gagnasnið

Formúluhönnuður ER hægt að nota til að skilgreina segð sem forsníður gögn sem er tekið úr gagnagjafa, þannig að gögn geta verið send sem hluti af myndandi rafrænu skjali. Ef þú ert með snið sem þarf að nota sem dæmigerða reglu sem þarf að endurnýta sem snið, geturðu lagt fram það snið það einu sinni í skilgreiningu sniðs sem umbreyting með heiti sem er með sniðsegð. Síðar þetta nefnda umbreyting er hægt að tengja við marga sniðhluti hvers úttak verður að vera sniðin í samræmi við stofnaða segð. Eftirfarandi skýringarmynd sýnir hönnun umbreytingar sem samanstendur af þessari gerð. Í þessu dæmi er **TrimmedString** umbreyting tekur gögn á innleið af gagnagerðinni **Strengur** gagnagerð, og stýfir bil í upphafi og enda þegar hann skilar aftur gildi strengsins. [![mynd umbreyting hönnun](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) eftirfarandi dæmi sýnir hvernig hægt er að nota umbreyting af þessari gerð. Í þessu dæmi eru margir þættir sniðs sem senda texta sem úttak í myndandi rafræna skjalið á keyrslutíma og vísa í **TrimmedString** umbreytingu eftir nafni. [![mynd umbreyting notkun](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Þegar íhlutir snið vísa í ** TrimmedString ** umbreyting (t.d. á **partyName** íhlutur í fyrrgreint sýnidæmi) þetta sendir texta sem úttak til að búa til skjal. Textinn inniheldur ekki bil fremst og aftast. Ef þú ert með snið sem þarf að nota eitt og sér, getur þú sett fram það snið sem einstaka segð bindingar fyrir tiltekna sniðsþáttinn. Eftirfarandi skýringarmynd sýnir segð sem samanstendur af þessari gerð. Í þessu dæmi er **partyType** sniðsþáttur bundin við gagnagjafa með segð sem umbreytir gögnum á innleið úr **Model.Company.RegistrationType** svæði í gagnagjafanum yfir í hástafa texta og sendir textann sem úttak til rafræna skjalið. [![mynd-bindingu-með-formúlu](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Vinnsla vinnsluflæðis

Formúluhönnuður rafrænnar skýrslugerðar er notuð til að skilgreina segðir sem eru notaðar til að stýra ferkusflæði fyrir myndun skjala: Hægt er að:

-   Skilgreina skilyrði til að ákvarða þegar þarf að stöðva ferli við myndun skjals
-   Tilgreina segðir sem mun stofna annaðhvort svarglugga fyrir endanotanda með skilaboð um stöðvaða vinnslu eða senda skilaboð aðgerðarskráningar um áframhaldandi ferli við myndun skýrslu.
-   Tilgreina skrárheiti myndandi skjala, og stjórna skilyrðum fyrir stofnun þeirra.

Hverja reglu fyrir flæðistýringu ferlis er hannað sem einstaka villuleit. Eftirfarandi skýringarmynd sýnir sannvottun af þessari gerð. Hér er skýring á skilgreiningunni í þessu dæmi:

-   Villuleit er metin þegar **INSTAT** hnútur er stofnaður í hinni myndandi xml-skrá.
-   Það stöðvar aðgerðarferlið um leið og það skilar **FALSE** ef listi yfir færslur er tómur
-   Sannvottunin skilar villuboð sem inniheldur texta merkis SYS70894 á tungumáli sem notandi kýs

[![mynd villuleit](./media/picture-validation.jpg)](./media/picture-validation.jpg) formúluhönnuður í SKAL má einnig nota til að tilgreina skráarnafn fyrir myndun rafrænna skjala og stýra stofnun skrá. Eftirfarandi skýringarmynd sýnir hönnun flæðistjórnunar ferlis sem samanstendur af þessari gerð. Hér er skýring á skilgreiningunni í þessu dæmi:

-   Listi yfir færslur úr **model.Intrastat** gagnagjafa er skipt í runur sem hver inniheldur allt að 1.000 færslur.
-   Úttak býr til ZIP-skrá sem inniheldur eina skrá í xml-snið fyrir hverja runu sem var stofnuð.
-   Segð gefur af sér skrárnafn til að mynda rafræn skjöl með því að tengja saman skráarheitið og nafnauki skráar. Fyrir aðra rönu og allar eftirfylgjandi runur inniheldur skráarheitið kenni runu sem nafnauka.
-   Segð er virkjar (með því að skilar til baka **TRUE **í) ferli skrármyndunar fyrir runurnar sem inniheldur minnst ein færsla

[![mynd skrá fjárhagsáætlunarstýringar](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Grunnmálskipan

Segðir rafrænnar skýrslugerðar geta innihaldið hverja sem er eða allar af eftirfarandi einingar:

-   Fastagildi
-   Virknitákn
-   Tilvísanir
-   Slóðir
-   Aðgerðir

#### <a name="constants"></a>Fastagildi

Þú getur notað texta og tölulega fastagildi (gildum sem ekki eru reiknaðar út) þegar þú hannar segðir. Til dæmis segðina ** GILDI ("100") + 20 ** notar tölur fasti 20 og streng fast "100" og skilar tölugildi **120**. Slepptar raðir eru studd í formúluhönnuði rafrænnar skýrslugerðar sem þýðir það þú getur tilgreina segðarstreng sem á að meðhöndla á annan hátt. Til dæmis, segðin **"Leo Tolstoy""War og Peace" "1 bindi"** skilar textastreng: **Leo Tolstoy "War og Peace" 1 bindi**

#### <a name="operators"></a>Virknitákn

Eftirfarandi tafla sýnir reiknitákn sem hægt er að nota til að framkvæma grundvallar stærðfræðilegar aðgerðum eins og viðbótar, frádráttur, deild og margföldun.

| Virki | Merking              | Dæmi |
|----------|----------------------|---------|
| +        | samlagning             | 1+2     |
| -        | Frádráttur Neitun | 5-2 -1  |
| \*       | Margföldun       | 7\*8    |
| /        | Skipting             | 9/3     |

Eftirfarandi tafla sýnir samanburðarreiknitákn sem eru studd, og sem er hægt að nota til að bera saman tvö gildi.

| Virki | Merking                  | Dæmi    |
|----------|--------------------------|------------|
| =        | Jafnt                    | X=Y        |
| &gt;     | Stærra en             | X&gt;Y     |
| &lt;     | Minna en                | X&lt;Y     |
| &gt;=    | Stærra en eða jafnt og | X&gt;=Y    |
| &lt;=    | Minna en eða jafnt og    | X&lt;=Y    |
| &lt;&gt; | Er ekki jafnt og             | X&lt;&gt;Y |

Þar að auki er hægt að notast við og-merki (&) sem samtengingu fyrir texta til að setja saman eða tengja saman einn eða fleiri textastrengi inn í einn stakan texta.

| Virki | Merking     | Dæmi                                        |
|----------|-------------|------------------------------------------------|
| &        | Samtengja | "Ekkert til að prenta" & ": " & "engar skráningar fundust" |

#### <a name="operator-precedence"></a>Forgangsröðun stjórnanda

Röðin sem hlutar samsettrar segðar eru metnir í er mikilvæg. Til dæmis niðurstaða segðar ** 1 + 4 / 2 ** eru mismunandi eftir því hvort aðgerð viðbót eða skiptingu aðgerð er framkvæmd fyrst. Hægt er að nota sviga til að skilgreina sérstaklega hvernig segð er metin. Til dæmis til að gefa til kynna að samlagningaraðgerðin ætti að framkvæma fyrst, er hægt að breyta fyrri segð í **(1 + 4) / 2**. Ef röð aðgerða sem þarf að framkvæma í segð er ekki skilgreindur sérstaklega, er röðin byggð upp á grundvelli sjálfgefins forgangs sem úthlutað er á studda virkja. Eftirfarandi töflur sýnir virkja og forgang sem úthlutað er á hvern og einn. Virkjar sem hafa hærri forgang (til dæmis 7) eru metnar á undan virkjum sem hafa lægri forgang (til dæmis 1).

| Forgangur | Virknitákn      | Málskipun                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Flokkun       | ( … )                                                    |
| 6          | Aðgangur meðlima  | … . …                                                    |
| 5          | Aðgerðakall  | … ( … )                                                  |
| 4          | Margfaldandi | … \* … … / …                                             |
| 3          | Viðbótarefni       | … + … … - …                                              |
| 2          | Samanburður     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Aðgreining     | … , …                                                    |

Virkjar í sömu línu hafa jafn forgangur. Ef segð inniheldur fleiri en eitt af þessum virkjar, er segðin metið úr vinstri til hægri. Til dæmis, er segðin **1 + 6 / 2 \*3 &gt;5** skilar **satt**. Ráðlagt að nota sviga til að tilgreina æskilega forgangsröð fyrir mat á segðir til að auðvelda segðir til að lesa og vinna með sérstaklega.

#### <a name="references"></a>Tilvísanir

Allar gagnaveitur núverandi þáttar rafrænnar skýrslugerðar (annað hvort líkan eða á sniði) sem eru tiltækir við hönnun segðar má nota sem tilvísanir með nafn. Til dæmis, gildandi gagnalíkan rafrænnar skýrslugerðar inniheldur **ReportingDate** gagnagjafann, sem skilar gildi gagnagerðar **DATETIME**. Rétt sníða gildið í mynda skjal, er hægt að vísa til gagnagjafa í segðinni sem hér segir: **DATETIMEFORMAT (ReportingDate, "dd-MM-áááá")** Öll tákn nafn þess tilvísun gagnagjafa sem standa ekki kreditbréfs í alphabet að koma á eftir eitt tilboð merki ('). Innihaldi heiti tilvísun gagnagjafa a.m.k. einn tákn sem standa ekki kreditbréfs alphabet (til dæmis greinamerkjasetningar merki eða önnur tákn skrifað), heiti þurfa vera innan tilvitnunarmerkja. Hér eru nokkur dæmi:

-   Gagnagjafanum **Today’s date & time** verður að vera nota í tilvísaðri segð rafrænnar skýrslugerðar sem hér segir: **'Today''s date & time’**
-   Aðferðin **name()** fyrir gagnagjafa **Viðskiptavinar** verður að vera tilvísað í segð rafrænnar skýrslugerðar sem hér segir: ** Customers.'name()'**

#### <a name="path"></a>Slóð

Þegar segð vísar í skipulögð gagnagjafa, geturðu nota skilgreiningu slóðar til að velja tiltekna frumstæðar einingu þess gagnagjafa. Stafurinn punktur (.) er notuð til að aðskilja einstakar einingar skipulagðs gagnagjafa. Til dæmis, gildandi gagnalíkan rafrænnar skýrslugerðar inniheldur **InvoiceTransactions** gagnagjafann, sem skilar lista yfir skráningar. Í ** InvoiceTransactions** skipulag skráninga inniheldur svæðin **AmountDebit** og **AmountCredit** sem tölugildi. Hægt er að hanna segð til að reikna út reikningsfærð upphæð sem hér segir: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Aðgerðir

Næsta hluta er fjallað um aðgerðir sem hægt er að nota í segðum rafrænnar skýrslugerðar. Allar gagnagjafar fyrir segðarsamhengi (núverandi gagnalíkan rafrænnar skýrslugerðar eða snið rafrænnar skýrslugerðar) auk fastagildi er hægt að nota sem færibreytur fyrir úthringiaðgerðir í samræmi við lista yfir rök úthringiaðgerða. Til dæmis, gildandi gagnalíkan rafrænnar skýrslugerðar inniheldur **InvoiceTransactions** gagnagjafann, sem skilar lista yfir skráningar. Í ** InvoiceTransactions** skipulag skráninga inniheldur svæðin **AmountDebit** og **AmountCredit** sem tölugildi. Hægt er að hanna segð til að reikna út reikningsfærð upphæð sem hér segir, en segðin getur notað innbyggða námundunar virkni rafrænnar skýrslugerðar: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Studdar aðgerðir
Eftirfarandi töflur útskýrir eiginleika fyrir breytingar á gögnum sem eru tiltækar fyrir hönnun á gagnalíkön rafrænnar skýrslugerðar og skýrslur rafrænnar skýrslugerðar. Þessi listi yfir aðgerðir er ekki föst og forritarar geta aukið við hann.. Til að sjá lista yfir aðgerðir sem þú getur notað, farðu í rúðuna aðgerðir í formúluhönnuður rafrænnar skýrslugerðar.

### <a name="date-and-time-functions"></a>Dagsetningar og tímavirkni

| Aðgerð                                   | Lýsing                                                                                                                                                                                                                                                                                                                                                      | Dæmi                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (dagsetning og tími, dagar)                   | Bæta tilgreindum dagafjölda við tilgreind datetime-gildi.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** skilar dagsetning og tími sjö daga fram í tímann.                                                                                                                                                                                                                            |
| DATETODATETIME (dagsetning)                      | Breyttu tilgreindu gildi dagsetningar í datetime-gildi.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. ' getCurrentDate()')** skilar gildandi Dynamics 365 fyrir setudagsetning 12/24/2015, sem **24/12/2015 12:00:00 F.H.**. Í þessu dæmi **CompInfo** er gagnagjafi rafrænnar skýrslugerðar fyrir **Dynamics 365 for Operations/Töflu** gerð sem vísar til í töflu CompanyInfo. |
| NOW ()                                     | Skila gildandi dagsetningu og tíma Dynamics 365 for Operations þjónn fyrir forrit sem datetime-gildi.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Skila gildandi dagsetningu og tíma Dynamics 365 for Operations þjónn sem dagsetningargildi.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Skilar gagnagildi með **núlli**.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Skilar datetime-gildi með **núlli**.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (datetime, format)          | Umbreyta tilgreinda datetime-gildi í streng á tilgreindu sniði. (Fyrir upplýsingar um studd snið sjá [staðlað](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** skilar núverandi Dynamics 365 for Operations þjónn fyrir forrit dagsetningu, 12/24/2015, sem **"24-12-2015"**, í samræmi við tilgreind sérstillt snið.                                                                                                          |
| DATETIMEFORMAT (datetime, format, culture) | Umbreyta tilgreinda dagsetningargildi í streng á tilgreindu sniði [menning](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Fyrir upplýsingar um studd snið sjá [staðlað](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** skilar núverandi Dynamics 365 for Operations þjónn fyrir forrit dagsetningu, 12/24/2015, sem **"24.12.2015"**, í samræmi við valda þýska menningu.                                                                                                             |
| SESSIONTODAY ()                            | Skila gildandi dagsetningu og tíma Dynamics 365 for Operations setudagsetning sem dagsetningargildi.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Skila gildandi dagsetningu og tíma Dynamics 365 for Operations setudagsetning og tíma sem datetime-gildi.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (dagsetning, snið)                  | Skilar strengjaframsetningu á dagsetningu sem notar tilgreint snið.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** skilar núverandi Dynamics 365 for Operations setudagsetningu, 12/24/2015, sem “**24-12-2015**”, í samræmi við tilgreind sérstillt snið.                                                                                                                      |
| DATEFORMAT (dagsetning, snið, menning)         | Umbreyta tilgreinda dagsetningargildi í streng á tilgreindu sniði og [menningu](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Fyrir upplýsingar um studd snið sjá [staðlað](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** skilar núverandi Dynamics 365 for Operations setudagsetningu, 12/24/2015, sem “**24.12.2015**”, í samræmi við valda þýska menningu.                                                                                                                       |

### <a name="list-functions"></a>Listavirkni

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Aðgerð</th>
<th>lýsing</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (input, length)</td>
<td>Skipta tilgreindum intaksstreng í undirstrengi, sem hvert um sig hefur tilgreinda lengd. Skila niðurstöðu sem nýja lista.</td>
<td><strong>SKIPTA (&quot;abcd&quot;, 3)</strong> skilar nýjum lista sem samanstendur af tveimur færslum sem hafa á <strong>STRENG</strong> svæði. Í fyrstu færslunni inniheldur texta <strong>&quot;abc&quot;</strong>, og í önnur færsla inniheldur texta <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (listi, númer)</td>
<td>Tilgreindur listi er skipt í runur sem hver inniheldur tilgreindan fjölda færslna. Skila niðurstöðu sem nýja lista yfir runur sem inniheldur eftirfarandi einingar:
<ul>
<li>Runur sem reglulegir listar (<strong>Gildi </strong> þáttur)</li>
<li>Núverandi rununúmer (<strong>BatchNumber </strong>þáttur)</li>
</ul></td>
<td>Í eftirfarandi dæmi er <strong>Línur</strong> gagnagjafa stofnaður sem listi yfir færslur fyrir þrjár færslur, sem er skipt í runur sem hver inniheldur allt að tvo færslur. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>Þetta sýnir snið hannað útlit þar sem bindingar til í <strong>Línur</strong> gagnagjafa eru stofnaðar til að mynda úttaks í xml-sniði sem sýnir einstaka hnúta fyrir hverja runu- og færslur í hana. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>Eftirfarandi er niðurstaða designed snið í gangi. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (record 1 [, record 2, ...])</td>
<td>Skila nýjum lista sem er myndaður úr tilgreindum frumbreytum.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> skilar tóm færsla, þar sem listi yfir reiti inniheldur alla reiti <strong>MainData</strong> og <strong>OtherData</strong> skráningar lista.</td>
</tr>
<tr class="even">
<td>LISTJOIN (list 1, list 2, ...)</td>
<td>Skila sameinuðum lista sem er myndaður úr listum úr tilgreindum frumbreytum.</td>
<td><strong>LISTJOIN (SKIPTA (&quot;abc&quot;, 1), skipta UPP (&quot;def&quot;, 1))</strong> skilar lista yfir sex færslur þar sem eitt svæði í <strong>STRENG</strong> gagnagerð inniheldur einn bókstafi.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (listi)</td>
<td>Skila <strong>SATT</strong> ef tilgreindur listi inniheldur ekki neinar einingar. Skila annars <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (listi)</td>
<td>Skila tómum lista með því að nota tilgreindan lista sem uppruna fyrir skipulag lista.</td>
<td><strong>EMPTYLIST (SKIPTA (&quot;abc&quot;, 1))</strong> skilar nýjum autt lista sem hefur sama skipulag sem listanum sem var skilað af <strong>SKIPTA</strong> aðgerð.</td>
</tr>
<tr class="odd">
<td>FIRST (listi)</td>
<td>Skila fyrsta færslan af tilgreindum lista,ef að sú færsla er ekki tómt. Annars er beitt undantekningu.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (list)</td>
<td>Skila fyrsta færslan af tilgreindum lista,ef að sú færsla er ekki tómt. Annars skal skila <strong>núll</strong> færslu.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (list)</td>
<td>Skilar lista sem inniheldur aðeins fyrsta atriði tilgreinds lista.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (path)</td>
<td>Skilar nýjum útflöttum lista sem nær til allra atriða sem hafa samsvörun við tilgreinda slóð. Slóð verður að vera skilgreint sem gild slóð gagnagjafa til einingar gagnagjafa af gagnagerðinni færslulisti. Slóð í streng, dagsetninguna, o. s. frv gagnaeiningar ættu að koma fram með villa á tíma hönnunar í segðasmiðsins rafrænnar skýrslugerðar.</td>
<td>Ef fært er inn <strong>SKIPTA (&quot;abcdef&quot;, 2)</strong> sem gagnagjafi (DS) <strong>TALNING (allitems BJÓST (DS. Gildi))</strong> skilar <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (listi [, segð 1, segð 2, …])</td>
<td>Skila tilgreinda lista sem er raðað í samræmi við tilgreindar frumbreytur sem hægt er að skilgreina sem segðir.</td>
<td>Þegar <strong>Lánardrottinn </strong>er skilgreindur sem gagnagjafi rafrænnar skýrslugerðar sem vísar til í töflu VendTable, <strong> ORDERBY (Lánardrottna, Vendors.'name()')</strong> skilar lista yfir lánardrottna sem er raðað eftir nafni í hækkandi röð.</td>
</tr>
<tr class="even">
<td>REVERSE (listi)</td>
<td>Skila tilgreindum lista í röð sem er afturábak.</td>
<td>Þegar <strong>Lánardrottins </strong>er skilgreind sem ER gagnagjafi sem vísar til í töflu VendTable<strong> REVERSE (ORDERBY (Lánardrottna, Vendors.'name()')) )</strong> skilar lista yfir lánardrottna sem er raðað eftir nafni í lækkandi röð.</td>
</tr>
<tr class="odd">
<td>WHERE (listi, skilyrði)</td>
<td>Skila tilgreinda lista sem er síaður í samræmi við tilgreindar skilyrði. Ólíkt aðgerinni <strong>SÍA</strong>, er tilgreind skilyrði er notað á listann í minni.</td>
<td>Þegar <strong>Lánardrottins</strong> er skilgreind sem ER gagnagjafi sem vísar til í töflu VendTable <strong>þar SEM (Lánardrottna, Vendors.VendGroup = &quot;40&quot;)</strong> skilar lista yfir lánardrottna sem tilheyra lánardrottnaflokk 40.</td>
</tr>
<tr class="even">
<td>ENUMERATE (listi)</td>
<td>Skila nýjum lista sem samanstendur af tölusettur færslur tilgreinds lista, og sem birtir eftirfarandi einingar:
<ul>
<li>Tilgreindar listaskráningar sem reglulegur listi(<strong>Gildi </strong> þáttur)</li>
<li>Gildandi færsluvísir (<strong>Númer </strong>þáttur)</li>
</ul></td>
<td>Í eftirfarandi dæmi er <strong>tölusettur</strong> gagnagjafa er stofnaður sem tölusettur listi yfir færslur lánardrottna úr á gagnagjafa <strong>Lánardrottna</strong> sem vísar á <strong>VendTable</strong> tafla. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Hér er snið, þar sem gögn bindingar eru stofnaðar til að mynda úttaks í xml-sniði sem sýnir einstaka lánardrottna sem tölusettur hnútar. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>Þetta er niðurstaða designed snið í gangi. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (listi)</td>
<td>Skila fjölda skráninga í tilgreindum lista, ef listinn er ekki tómur. Skila annars <strong>0</strong> (núll).</td>
<td><strong>FJÖLDI (SKIPTA (&quot;abcd&quot;, 3))</strong> skilar <strong>2</strong>, þar sem <strong>SKIPTA</strong> aðgerð býr til lista sem samanstendur af tveimur færslum.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (slóð)</td>
<td>Skilar færslulista sem búinn er til úr frumbreytu af einni af eftirfarandi gerð:
<ul>
<li>Tölusetning líkans</li>
<li>Tölusetning sniðs</li>
<li>Gámur</li>
</ul>
Listinn sem er búinn til samanstendur af færslum með eftirfarandi svæði:
<ul>
<li>Nafn</li>
<li>Merkimiði</li>
<li>lýsing</li>
</ul>
Svæðin Merkimiði og Lýsing skila gildum á keyrslutíma á grunni tungumálastillinga sniðsins.</td>
<td>Eftirfarandi dæmi sýnir tölusetning í gagnalíkan. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Eftirfarandi dæmi sýnir:
<ul>
<li>Tölusetning líkans sett inn í skýrslu sem gagnagjafa.</li>
<li>Segð rafrænnar skýrslugerðar hannað til að nota tölusetning líkans sem færibreytu fyrir þessa aðgerð.</li>
<li>Gagnagjafi af gerðinni færslulisti settur inn í skýrslu með því að nota stofnaða segð rafrænnar skýrslugerðar.</li>
</ul><ph id="t1">
< til href="./media/ger-listoffields-function-in-format-expression.png" ></ph><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> eftirfarandi dæmi sýnir ER snið einingar sem eru bundnar við gagnagjafa færsluskrár gerð sem voru stofnaðar með aðgerðinni LISTOFFIELDS. <a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Þetta er niðurstaða hannað snið framkvæmd. <a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Athugasemd:</strong> fyllt Translated texti fyrir merkimiða og lýsingar á úttak snið ER samkvæmt tungumálastillingar skilgreindur fyrir SKRÁ yfir- og MÖPPU snið einingar.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (listanum, svæðisheiti, skiltákn)</td>
<td>Skilar streng samtengdra gilda reist úr lista sem er aðskilinn með völdu skiltákni.</td>
<td>Ef þú færðir inn SPLIT(“abc” , 1) sem gagnagjafa DS, segðin STRINGJOIN (DS, DS.Value, “:”) gefur til baka“a:b:c”</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (listanum, markgildi, uppruni marks)</td>
<td>Skiptir uppgefins lista yfir í nýja lista yfir undirlista og skilar niðurstöðum með innihaldi færslulista. Færibreyta markgildis tilgreinir gildi marksins sem á að skipta upprunalistanum. Færibreyta uppruna marks tilgreinir þrepið sem heildarsamtalan eykst um. Markinu er ekki beitt á staka vöru á tilteknum lista þegar uppruni marsk fer fram yfir tilgreint mark.</td>
<td>Eftirfarandi dæmi sýnir dæmi um snið með gagnagjafa. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Þetta er niðurstaða snið framkvæmdar sem sýnir flatur listi yfir atriði grunnvöru. <a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>Eftirfarandi dæmi sýnir sama sniðsins sem var leiðrétt til að birta lista yfir atriði grunnvöru í runum þegar einn rununa verður að innihalda grunnvörur sérstakrar með heildarþyngd sem ekki ætti að vera yfir hámarki 9. <a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Þetta er niðurstaða leiðrétt snið framkvæmd. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Athugasemd:</strong> marka er ekki notuð í síðasta vara uppruna lista sem gildi (11) frumkóða hans mörk (þyngd) yfir skilgreinda mörkum (9). Notið annað hvort virkninga <strong>WHERE </strong> eða <strong>Virkt</strong> segð samsvarandi sniðseiningar til að hunsa (sleppa) undirlistum þegar verið er að mynda skýrslur(ef þörf krefur).</td>
</tr>
<tr class="odd">
<td>Afmörkun (listi, skilyrði)</td>
<td>Skilar tilteknum lista síuð fyrir tilgreind skilyrði með því að breyta fyrirspurninni. Ólíkt <strong>WHERE</strong> aðgerð, er tilgreind skilyrði notað á stigi gagnagrunns fyrir hvaða gagnagjafa rafrænnar skýrslugerðar af gerðinni færslur Töflu.</td>
<td>SÍA (Lánardrottna, Vendors.VendGroup = &quot;40&quot;) skilar lista yfir aðeins lánardrottna sem tilheyra flokki á lánardrottna "40" þegar <strong>Lánardrottins</strong> er skilgreindur sem gagnagjafi ER vísað til í <strong>VendTable</strong> töflu</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Rökvirkni

| Aðgerð                                                                                | lýsing                                                                                                                                                                                                                                                                     | Dæmi                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MÁL (segðina, valkosturinn 1, til þess að 1 \[valkosturinn 2, til þess að 2\] ... \[, sjálfgefna niðurstöðu\]) | Meta tilgreind gildi segðar gagnvart tilgreindum öðrum valkostum. Skila niðurstöðu valkostarins sem er jafngild gildi segðarinnar. Annars, skila sjálfgefna niðurstöðu sem var valkvætt færð inn (síðasta færibreyta sem ekki kemur valkostur á undan). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** skilar strengnum **"WINTER"** þegar núverandi seta Dynamics 365 for Operations dagsetningar er á milli október og desember. Annars skilar það auður strengur. |
| IF (skilyrði, gildið 1, gildi 2)                                                        | Skila tilgreinda gildið 1 þegar ákveðið skilyrði er uppfyllt. Annars skilagildi 2. Gildið 1 og 2 gildi eru færslur eða skrá lista yfir niðurstöður hafa einungis svæði sem eru til í báðum lista.                                                                     | **EF (1 = 2 "skilyrði er uppfyllt", "skilyrði er ekki í uppfyllt")** skilar strengurinn **"skilyrði er ekki uppfyllt"**.                                                                                                                                                      |
| NOT (ástand)                                                                         | Skila öfugu röklega gildi tilgreinds skilyrðis.                                                                                                                                                                                                                   | **NOT (TRUE)** skilar **FALSE**.                                                                                                                                                                                                                            |
| OG (skilyrðið 1\[, skilyrðið 2,... \])                                                 | Skilar **TRUE** ef *öll *tilgreind skilyrði eru uppfyllt. Skila annars **FALSE**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** skilar **TRUE**. **AND (1=2, "a"="a")** skilar **FALSE**.                                                                                                                                                                           |
| EÐA (skilyrðið 1\[, skilyrðið 2,... \])                                                  | Skila **FALSE** ef *allar * tilgreind skilyrði eru röng. Skila **TRUE** ef *allar *tilgreind skilyrði eru sönn.                                                                                                                                                                 | **OR (1=2, "a"="a")** skilar **TRUE**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Reikniaðgerðir

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Aðgerð</th>
<th>Lýsing</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (númer)</td>
<td>Skilar algildi tilgreindrar tölu, (talan án tákns síns).</td>
<td><strong>ABS (-1)</strong> skilar <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (númer, valdheimild)</td>
<td>Skilan niðurstöðum af því að hækka tilgreinda jákvæða tölu upp að tilgreindri valdheimild.</td>
<td><strong>POWER (10, 2)</strong> skilar <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (streng aukastaf, skiltákn stafaflokkunar)</td>
<td>Umbreyta strengnum í númer. Tilgreind tákn er notað til að aðgreina heiltala og tugastafi í tugabroti og tilgreinda skiltákn fyrir þúsund eru einnig notaðar.</td>
<td><strong>NUMBERVALUE (&quot;1 234,56&quot;, &quot;,&quot;, &quot;&quot;)</strong> skilar gildinu <strong>1234.56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (strengur)</td>
<td>Umbreyta strengnum í númer. Kommur og punktar (.) og skoðast sem skiltákn aukastafa, og bandstrik fremst (-) er notað sem neikvætt formerki. Beittu undantekningu ef öðrum stafir sem ekki eru tölur koma upp í tilgreindum streng.</td>
<td><strong>GILDI (&quot;1 234,56&quot;)</strong> throws undantekningu.</td>
</tr>
<tr class="odd">
<td>ROUND (númer, aukastafir)</td>
<td>Skila tilgreindu númeri, sem er sléttað upp að tilgreindum fjölda aukastafa:
<ul>
<li>Ef gildið tilgreind fjöldi aukastafa er meira en 0 (núll) er tilgreind talan er sléttuð að tilgreindum fjölda aukastafa.</li>
<li>Ef tilgreint gildi aukastafa er 0 (núll), er tiltekinn númer sléttuð að næsta heiltala.</li>
<li>Ef tilgreint gildi aukastafa er minna en 0 (núll), er tiltekinn númer sléttuð til vinstri við tugastafinn.</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> sléttar tvo aukastafi og skilar <strong>1200.77</strong>. <strong>ROUND (1200.767, -3)</strong> sléttar næsta margfeldi svæðisins 1.000 og skilar <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (númer, aukastafir)</td>
<td>Skila tilgreindu númeri, sem er sléttað niður (í átt að núll) upp að tilgreindum fjölda aukastafa: <strong>Athugasemd:</strong> Þessa aðgerð hegðar sér eins og <strong>ROUND</strong>, en það sléttar alltaf tiltekin númer niður á við.</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> sléttar niður á við tvo aukastafi og skilar <strong>1200.76</strong>. <strong>ROUNDDOWN (1700.767, -3)</strong> sléttar niður á við næsta margfeldi svæðisins 1.000 og skilar <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (númer, aukastafir)</td>
<td>Skila tilgreindu númeri, sem er sléttað upp (burt frá núll) að tilgreindum fjölda aukastafa: <strong>Athugasemd:</strong> Þessa aðgerð hegðar sér eins og <strong>ROUND</strong>, en það sléttar alltaf tiltekin númer upp á við.</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> sléttar upp að tvo aukastafi og skilar <strong>1200.77</strong>. <strong>ROUNDUP (1200.767, -3)</strong> sléttar upp að næsta margfeldi svæðisins 1.000 og skilar <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

### <a name="record-functions"></a>Færsluvirkni

| Aðgerð             | Lýsing                                                                                                                                                                                                                                     | Dæmi                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (listi) | Skila **núll** færslu sem hefur sömu skipan og tilgreind færsluskrár eða færsla. **Athugasemd: **Þessa aðgerð er úreltur. Notið **EMPTYRECORD** í staðinn.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** skilar nýja tóma skráningu sem hefur sömu skipan sem listanum sem var skilað af **SPLIT** aðgerð. |
| EMPTYRECORD (skráning) | Skila **núll** færslu sem hefur sömu skipan og tilgreind færsluskrár eða færsla. **Athugasemd:** A **núll** færslu þar sem öll svæði hafa autt gildi að færslan sé (**0**\[núll\] fyrir tölur, auður strengur strengir og svo framvegis). | **EMPTYRECORD (SPLIT ("abc", 1))** skilar nýja tóma lista sem hefur sömu skipan sem listanum sem var skilað af **SPLIT** aðgerð.   |

### <a name="text-functions"></a>Textavirkni

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Aðgerð</th>
<th>Lýsing</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (strengur)</td>
<td>Skila tilgreinda streng sem er breytt í hástafi.</td>
<td><strong>EFRI (&quot;Sýnishorn&quot;)</strong> skilar <strong>&quot;SÝNISHORN&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (strengur)</td>
<td>Skila tilgreinda streng sem er breytt í lágstafi.</td>
<td><strong>NEÐRI (&quot;Sýnishorn&quot;)</strong> skilar <strong>&quot;sýnishorn&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (streng, fjölda stafa)</td>
<td>Skilar tilteknum fjölda stafa úr upphafi tiltekins strengs.</td>
<td><strong>VINSTRI (&quot;Sýnishorn&quot;, 3)</strong> skilar <strong>&quot;Samúel&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (streng, fjölda stafa)</td>
<td>Skilar tilteknum fjölda stafa úr enda tiltekins strengs.</td>
<td><strong>HÆGRI (&quot;Sýnishorn&quot;, 3)</strong> skilar <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (streng, byrjunarstöðu, fjölda stafa )</td>
<td>Skilar tilteknum fjölda stafa úr enda tiltekins strengs, og byrjar í tiltekinni stöðu.</td>
<td><strong>MIÐUR (&quot;Sýnishorn&quot;, 2, 3)</strong> skilar <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (strengur)</td>
<td>Skilar fjölda stafa í tilteknum streng..</td>
<td><strong>LEN (&quot;Sýnishorn&quot;)</strong> skilar <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (númer)</td>
<td>Skila streng af stöfum sem vísað er til með tilgreinda Unicode númerinu.</td>
<td><strong>STAF (255)</strong> skilar <strong>&quot;ÿ&quot;</strong>. <strong>Athugasemd:</strong> Skilað streng fer eftir dulritun sem valinn er í yfireiningu SKRÁR-sniðs. Listi yfir studda kóðun má finna í <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Dulritunarflokkur</a> efnisatriði.</td>
</tr>
<tr class="even">
<td>CONCATENATE (string 1 [, string 2, …])</td>
<td>Skila öllum tilgreinda textastrengi, sem eru tengdar í streng einn.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> skilar <strong>&quot;abcdef&quot;</strong>. <strong>Athugasemd:</strong> segðin <strong>&quot;abc&quot;&amp;&quot;def&quot;</strong> einnig skilar <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (strengur mynstur, útskipting)</td>
<td>Skila tilgreindum strengur, þar sem öll tilfelli stafa í tilgreindu mynstri strengs koma í stað stafa á tilsvarandi stöðu tilgreinda strengsins sem skiptir út.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> kemur í stað mynstrið <strong>&quot;cd&quot;</strong> með strengnum <strong>&quot;GH&quot;</strong> og skilar <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (streng, mynstur, útskipting, er flagg fyrir reglulega segð)</td>
<td>Þegar tilgreint flagg reglulegrar segðar er <strong>satt</strong>, skila tilgreint streng sem er breytt með því að nota reglulega segðin sem er tilgreindur sem mynstur frumbreytu fyrir þessa aðgerð. Þessi segð er notuð til að finna stafi sem verður að skipta út. Stafir tilgreindrar frumbreytu eru notaðar til að skipta út stöfum sem finnast. Regluleg tilgreint flatt reglulegrar segðar er <strong>rangt</strong>, hegðar þessi virkni sér eins og <strong>TRANSLATE</strong>.</td>
<td>  <strong>Skipta ÚT (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, satt)</strong> á regluleg segð sem fjarlægir öll tákn ekki töludálkur og skilar <strong>&quot;19234564971&quot;</strong>. <strong>Skipta ÚT (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, rangt)</strong> skuldfært á mynstur <strong>&quot;cd&quot;</strong> með strengnum <strong>&quot;GH&quot;</strong> og skilar <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (inntak)</td>
<td>Skila tilgreind inntak, sem umbreytt er í textastreng er forsniðið samkvæmt landsstaðli þjóns fyrir gildandi tilvik Dynamics 365 for Operations. Fyrir gildi í af gerðinni <strong>real</strong> ,umreikning strengs takmarkast við sem nemur tveimur tugasætum.</td>
<td>Ef Dynamics 365 fyrir Aðgerðir þjónsstaðsetninga tilvik er skilgreindur sem <strong>IS-IS</strong>, <strong>TEXTA (NÚ ())</strong> skilar gildandi Dynamics 365 fyrir setudagsetning 12/17/2015, texti streng <strong>&quot;17/12/2015 07:59:23 F.H.&quot;</strong>. <strong>TEXTI (1/3)</strong> skilar <strong>&quot;0,33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (string 1, string 2[, string 3, ...])</td>
<td>Skila tilgreint streng sem er sniðin með því að skipta út öllum tilvikum af allar tilvika á að skila <strong>%N</strong> með <em>n</em>th frumbreytu. Frumbreytur eru strengir. Ef frumbreyta er ekki gefin upp fyrir færibreytu færibreytan er skilað sem <strong>&quot;%N&quot;</strong> í strengnum. Fyrir gildi í af gerðinni <strong>real</strong> ,umreikning strengs takmarkast við sem nemur tveimur tugasætum.</td>
<td>Í þessu dæmi skilar <strong>PaymentModel</strong> gagnagjafi lista yfir færslur viðskiptavina með þætti <strong>Viðskiptavinar</strong> og gildi vinnsludagsetningar með <strong>ProcessingDate</strong> svæði. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>ER sniði sem er hannað til að mynda rafræna skrá fyrir valda viðskiptavini <strong>PaymentModel</strong> er valinn sem gagnagjafa og stýrir flæði ferli. Gerð er undantekning fyrir endanotendur þegar valinn viðskiptavinur er stöðvað af dagsetning þegar skýrslan er unnin. Formúlu sem er hannað fyrir þessa gerð vinnslustýringar getur notað eftirfarandi tilföng:
<ul>
<li>Dynamics 365 for Operations merki SYS70894 sem hefur eftirfarandi texta:
<ul>
<li><strong>Fyrir tungumál IS-IS:</strong>&quot;Ekkert til að prenta&quot;</li>
<li><strong>Fyrir DE tungumál:</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operations merki SYS18389 sem hefur eftirfarandi texta:
<ul>
<li><strong>Fyrir tungumál IS-IS:</strong>&quot;Viðskiptavinur %1 er lokaður fyrir %2.&quot;</li>
<li><strong>Fyrir tungumálið DE:</strong>&quot;gesperrt für %2 í wird Debitor '%1'.&quot;</li>
</ul></li>
</ul>
Er formúlunnar sem hægt er að hanna hér: SNIÐI (CONCATENATE (@&quot;SYS70894&quot;,&quot;. &quot;@&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (líkan. ProcessingDate, &quot;d&quot;)) Ef unnið er úr skýrslu fyrir á <strong>viðskiptavinar Smásölu Litware</strong> á 17 Desember 2015 í á <strong>IS-IS</strong> menning og <strong>IS-IS</strong> tungumál, þessa formúlu skilar eftirfarandi texta sem er hægt að birtast sem undantekning skilaboð fyrir notandinn: &quot;Ekkert til að prenta. Viðskiptavinur Litware Smásölu er lokaður fyrir 17/12/2015.&quot; Ef unnið er úr sömu skýrslu fyrir á<strong> Litware Retail viðskiptavinar</strong> á 17 Desember 2015 í á <strong>DE</strong> menning og <strong>DE</strong> tungumál, þessa formúlu skilar eftirfarandi texta sem notar snið mismunandi dagsetningar: &quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot; <strong>Athugasemd: </strong>eftirfarandi málskipun er notað í formúlum rafrænnar skýrslugerðar fyrir merki:
<ul>
<li><strong>Fyrir merki úr Dynamics 365 rekstrartilföngum:</strong> <strong>@&quot;X&quot;</strong>, þar sem X er Merkiskenni í Hugbúnaðarhlutatrénu (AOT)</li>
<li><strong>Fyrir merki sem eru í ER skilgreiningar:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, þar sem X er á Kenni tungumáls í skilgreiningunni ER</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (númer, snið)</td>
<td>Skilar málsvari strengs fyrir tiltekið númer í tilteknu sniði. (Sjá upplýsingar um studd snið <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">stöðluðum</a> og <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">sérsniðna</a>.) Samhengi sem þessi aðgerð er keyrð í ákvarðar þá menningu sem er notuð til að sníða vörunúmer.</td>
<td>Fyrir þá menningu IS-IS <strong>NUMBERFORMAT (0,45 &quot;p&quot;)</strong> skilar <strong>&quot;45,00%&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> skilar <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (númer, tungumál, gjaldmiðil, prenta flaggheiti gjaldmiðils, tugakomma)</td>
<td>Skilar númer sem er stafað (umbreytt) í textastrengi á tilgreinda tungumálið. Tungumálskóði er valfrjáls: þegar hann er skilgreindur sem auður strengur verður hlaupandi tungumálakóði samhengis (skilgreind fyrir myndandi möppu eða skrá) notuð í staðinn. Gjaldmiðilskóðinn er valkostur. Gjaldmiðill fyrirtækisins er tekið þegar hann er skilgreindur sem tómur strengur. Athugið, <strong>Prenta heiti gjaldmiðils</strong> færibreyta og <strong>tugakommur</strong> færibreyta eru greind í eftirfarandi tungumálakóðum aðeins: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Athugið, <strong>Prenta heiti gjaldmiðils</strong> færibreyta er greina aðeins fyrir Dynamics 365 for Operations fyrir fyrirtæki með samhengi lands sem styður gjaldmiðilsfrávik.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;IS&quot;, &quot;&quot;, false, 2) skilar "Eitt Þúsund Tveggja Hundrað Thirty Fjögur og 56" NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) "Sto dwadzieścia" skilar NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, satt 2) skilar "Сто двадцать евро 21 евроцент"</td>
</tr>
<tr class="odd">
<td>PADLEFT (strengur, lengd, stafir til fyllingar)</td>
<td>Skilar streng í tilgreindri lengd þar sem upphafið á núgildandi streng er fyllt með tilgreindum stöfum.</td>
<td>PADLEFT (“1234”, 10,““) skilar textastreng “1234”</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Gagnasöfnunaraðgerðir

Aðgerð

lýsing

Dæmi

FORMATELEMENTNAME ()

Skilar heiti einingar núgildandi sniðs Skilar TÓMUR Strengur þegar slökkt er á flagginu **Safna saman upplýsingum um framleiðslu** í núgildandi skrám.

Vísað er í **Rafræn skýrslugerð nota gögn sniðúttaks til að telja og legja saman** (hluti í **Komast yfir/hanna íhluti upplýsingatækniþjónustu/-lausna** viðskiptaferli) leiðarvísi fyrir Verk til að læra meira um notkun þessar aðgerðir .

SUMIFS (lykill streng fyrir samlagningu, skilyrði range1 streng skilyrði gildi1 streng \[, skilyrði range2 streng, skilyrði gildi2 strengur... \])

Skilar summu af gildum xml-hnúta (með heiti skilgreint sem lykil) sem hefur verið safnað í þessari framkvæmd sniðs og sem uppfylla skilyrðin sem færð voru inn (samstæður sviðs og gildis). Skilar núllgildi þegar slökkt er á flagginu **Safna saman upplýsingum um framleiðslu** í núgildandi skrám.

SUMIF (lykilstreng fyrir samlagningu strengur, strengur skilyrðasviðs, strengur skilyrðagilda...])

Skilar summu af gildum xml-hnúta (með heiti skilgreint sem lykil) sem hefur verið safnað í þessari framkvæmd sniðs og sem uppfylla skilyrðin sem færð voru inn (sviðs og gildis). Skilar núllgildi þegar slökkt er á flagginu **Safna saman upplýsingum um framleiðslu** í núgildandi skrám.

COUNTIFS (streng range1 skilyrði, skilyrði gildi1 streng \[, skilyrði range2 streng, skilyrði gildi2 strengur... \])

Skilar fjölda xml-hnúta sem hefur verið safnað meðan á þessari framkvæmd sniðs stóð og sem uppfyllir skilyrðin sem færð voru inn (samstæður sviðs og gildis). Skilar núllgildi þegar slökkt er á flagginu **Safna saman upplýsingum um framleiðslu** í núgildandi skrám.

COUNTIF (strengur skilyrðasviðs, strengur skilyrðagildis)

Skilar fjölda xml-hnúta sem hefur verið safnað meðan á þessari framkvæmd sniðs stóð og sem uppfyllir skilyrðin sem færð voru inn (sviðs og gildis). Skilar núllgildi þegar slökkt er á flagginu **Safna saman upplýsingum um framleiðslu** í núgildandi skrám.

COLLECTEDLIST (streng range1 skilyrði, skilyrði gildi1 streng \[, skilyrði range2 streng, skilyrði gildi2 strengur... \])

Skilar lista yfir gildi xml-hnúta sem hefur verið safnað meðan á þessari framkvæmd sniðs stóð og sem uppfyllir skilyrðin sem færð voru inn (sviðs og gildis). Skilar auðum lista þegar slökkt er á flagginu **Safna saman upplýsingum um framleiðslu** í núgildandi skrám.

### <a name="other-business-domainspecific-functions"></a>Other (lénsértæk virkni fyrir viðskipti)

| Aðgerð                                                                         | lýsing                                                                                                                                                                                                                                                        | Dæmi                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (upphæð, frumgjaldmiðils, mark gjaldmiðil, dagsetning, fyrirtækisins)        | Umreikna tilgreinda peningaupphæð úr upprunagjaldmiðli í markgjaldmiðil með því að nota stillingar fyrir tilgreindan Dynamics 365 for Operations fyrirtækið á tilgreindri dagsetningu.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** skilar jafngildi einni evru í Bandarískum dollurum á dagsetningu núverandi setu, byggða á stillingum DEMF-fyrirtækisins.                                                                                                                                  |
| ROUNDAMOUNT (tölu, aukastafi, sléttunarreglu)                                       | Slétta tilgreinda upphæð samkvæmt tilgreindri sléttunarreglan og tilgreindum fjölda aukastafa. **Athugasemd:** tilgreina verður sléttunarreglan sem gildi í Dynamics 365 for Operations **RoundOffType** tölusetning.                          | Ef í **líkan. RoundOff** færibreyta er stillt á *** Downward ***, **ROUNDAMOUNT (1000.787, 2, virðislíkan. RoundOff)** skilar gildinu **1000.78**. Ef **model.RoundOff** færibreyta er stillt á annað hvort **Venjuleg** eða **Sléttun**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** skilar gildinu **1000.79**. |
| CURCredRef (tölur)                                                              | Skila Tilvísun lánardrottins, byggt á tölustöfum í tilgreint reikningsnúmeri.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** skilar **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (tölur)                                                                 | Skila Tilvísun lánardrottins, sem MOD97 segð, byggt á tölustöfum tilgreinds reikningsnúmers.                                                                                                                                                            | **MOD\_97 ("LÁNARDROTTINS-200002")** skilar **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef  (tölur)                                                              | Skila ISO Tilvísun lánardrottins, byggt á tölustöfum stafrófstáknum í tilgreint reikningsnúmeri. **Athugasemd: **til Að útiloka tákn úr stafrófi sem ekki eru í samræmi við ISO, inntaks færibreytan verður að þýða áður en hún er send til þessa aðgerð. | **ISOCredRef ("VEND-200002")** skilar **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (streng, númer)                                  | Sækja fjárhagsleg viðbótarvíddarkenni Víddir eru sýndir í þennan streng sem Kenni aðgreindir með kommum. Númer skilgreina umbeðin raðnúmer víddar í þennan streng.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA BB, CC, DD, EE, FF, GG, HH", 3) skila "CC"                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Skilar kóða núverandi skráðs fyrirtækisins.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_BANKANS\_MOD\_10 (tölur)                                                       | Skila Tilvísun lánardrottins, sem MOD10 segð, byggt á tölustöfum gefins reikningsnúmers.                                                                                                                                                                      | CH\_BANKANS\_MOD\_10 ("LÁNARDROTTINS-200002") skilar 3                                                                                                                                                                                                                                                                   |
| FA\_SAMTALA (föst eign kóða, kóðagildið líkan, upphafsdagsetningu, lokadagsetningu)               | Skilar tilbúnum gagnageymi með stöðu eigna fyrir ákveðið tímabil.                                                                                                                                                                                         | FA\_SAMTALA ("COMP-000001", "Núverandi", Date1 er Date2) skilar undirbúin gagnahólf eignarinnar "COMP-000001" með gildið "Núverandi" fyrir tímabil úr Date1 í Date2.                                                                                                                        |
| Eigna\_STÖÐU (fastra eigna kóði, virði kóði framleiðslulíkans, skýrslugerðarár, reikningsskiladegi) | Skilar tilbúnum gagnageymi með stöðu eigna. Skýrslugerðarár verður að tilgreina sem gildi í Dynamics 365 for Operations **AssetYear** tölusetning.                                                                                           | FA\_SAMTALA ("COMP-000001", "Núverandi", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) skilar undirbúin gagnahólf innistæðum eignarinnar "COMP-000001" með gildið "Núverandi" á gildandi 365 aðgerða setudagsetning.                                                                |

### <a name="functions-list-extension"></a>Viðbót við lista yfir virkni

Rafræn skýrslugerð styður möguleikann á að útvíkka listann yfir aðgerðir sem eru notaðar í segðir rafrænnar skýrslugerðar. Þetta krefst dálítillar verkfræðikunnáttu. Fyrir ítarlegar upplýsingar sjá [Útvíkka listann fyrir aðgerðir rafrænnar skýrslugerðar](general-electronic-reporting-formulas-list-extension.md)

<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Útvíkka listann yfir aðgerðir Rafrænnar skýrslugerðar](general-electronic-reporting-formulas-list-extension.md)


