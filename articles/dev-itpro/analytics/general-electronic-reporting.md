---
title: "Rafræn skýrslugerð (ER)"
description: "Í þessari grein er að finna yfirlit yfir verkfærið „Rafræn skýrslugerð“. Þar á meðal er að finna upplýsingar um lykilhugtök, sviðsmyndir sem Rafræn skýrslugerð styður og lista yfir snið sem hafa verið hönnuð og gefin út sem hluti af lausninni."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 99c10649d7683265fcac86c1825c5a965bbdb415
ms.openlocfilehash: f27f228e48da653a9caf666f9053fe45a7c23745
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---

# <a name="electronic-reporting-er"></a>Rafræn skýrslugerð (ER)

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna yfirlit yfir verkfærið „Rafræn skýrslugerð“. Þar á meðal er að finna upplýsingar um lykilhugtök, sviðsmyndir sem Rafræn skýrslugerð styður og lista yfir snið sem hafa verið hönnuð og gefin út sem hluti af lausninni.

Rafræn skýrslugerð (ER) er verkfæri sem hægt er að nota til að skilgreina sniðið á rafrænum skjölum á innleið og útleið í samræmi við ákvæði laga mismunandi landa/svæða. ER (rafræn skýrslugerð) gerir þér kleift að stjórna þessum sniðum í lífsferli þeirra. Til dæmis er hægt að taka upp nýjar lagalegar kröfur, og búa til viðskiptaskjöl á tilskildu sniði til að skiptast rafrænt á upplýsingum við stjórnvöld, banka og fleiri aðila.

Vélar fyrir rafræna skýrslugerð eru ætlaðar fyrir viðskiptanotendur í stað þróara. Þar sem þú skilgreinir snið en ekki kóða eru ferlin við að stofna og stilla snið fyrir rafræn skjöl hraðvirkari og auðveldari.

ER styður eins og er TEXT, XML, Microsoft Word skjöl og OPENXML vinnublaðssnið. Hins vegar veitir viðbótarviðmót stuðning við fleiri snið.

## <a name="capabilities"></a>Geta
ER-vélin hefur eftirfarandi getu:

- Hún er eitt samnýtt verkfæri til rafrænnar skýrslugerðar á mismunandi sviðum, og kemur í stað 20 mismunandi véla sem gera einhvers konar rafræna skýrslugerð fyrir Microsoft Dynamics 365 for Finance and Operations.
- Það gerir snið á skýrslu einangrað frá núgildandi innleiðingu Finance and Operations. Með öðrum orðum gildir sniðið fyrir mismunandi útgáfur af Finance and Operations.
- Hann styður stofnun sérsniðinnar sniða sem byggð er á upprunalegu sniði. Það felur einnig í sér getu til að uppfæra sjálfkrafa sérhönnuð snið þegar breytingar á upprunalegu sniði eiga sér stað, vegna krafna um staðfærslu/sérsnið.
- Verður það aðal viðtekna verkfærið til að styða við kröfur um staðfæringu í rafrænni skýrslugerð – bæði fyrir Microsoft sem og microsoft samstarfsaðila;
- Það styður getu til að dreifa sniðum til viðskiptaaðila og viðskiptavini með Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Lykilhugtök
### <a name="components"></a>Íhlutir

ER styður tvær gerðir íhluta **gagnalíkan** og **Snið**.

#### <a name="data-model-components"></a>Íhlutir gagnalíkana

Þáttur gagnalíkans er óhlutbundin framsetning á gagnaskipulagi. Hann er notaður til að lýsa tilteknu viðskiptasviði með nægilegum upplýsingum til að tilkynningaskylda fyrir það svið sé uppfyllt. Íhlutir gagnalíkans samanstendur af eftirfarandi hluta:

- Gagnalíkan sem hópur af viðskiptaeiningum fyrir tiltekin svið auk stigskiptra tengslaskilgreininga á milli þessara eininga.
- Líkanavörpun sem tengir valda Finance and Operations gagnagjafa við einstakar einingar gagnalíkans sem tilgreinir, í keyrslutíma, gagnaflæði og reglur viðskiptagagna við þætti gagnalíkans.

Viðskiptaeining gagnalíkans er birt sem geymir (skýrsla). Eiginleikar viðskiptaeininga eru sýndir sem gagnaatriði (svæði). Hvert gagnaatriði hefur einstakt heiti, merki, lýsingu og gildi. Hægt er að hanna virði hvers atriðis svo það sé viðurkennt sem strengur, heiltala, raunverulegt, dagsetning, tölusett, Boole-gildi o.s.frv. Þar að auki getur það verið önnur færsla eða færslulisti.

Einstakur þáttur gagnalíkans getur innihaldið mörg stigveldi sviða sem eru tilgreind eftir viðskiptaeiningum. Einnig getur hann innihaldið líkanavarpanir sem styðja skýrslutengt gagnaflæði á keyrslutíma. Stigveldin verða aðgreind eftir einni færslu sem hefur verið valin sem rót líkanavörpunar. Til dæmis, Gagnalíkan fyrir greiðslusvið gæti stutt eftirfarandi varpanir:

- Fyrirtæki \> Lánardrottinn \> Greiðslufærslur AP-sviðs
- Viðskiptavinur \> Fyrirtæki \> Greiðslufærslur AR-sviðs

Athugið að viðskiptaeiningar, eins og fyrirtæki og greiðslufærslur, eru búnar til einu sinni. Mismunandi varpanir endurnota þær svo.

Líkanavörpun sem styður rafræn skjöl á útleið hefur eftirfarandi getu:

- Hægt er að nota mismunandi gagnagerðir Finance and Operations sem gagnagjafa fyrir gagnalíkan. Til dæmis getur það notað töflur, gagnaeiningar, aðferðir eða upptalningar.
- Það styður ílagsfæribreytur notanda sem má skilgreina sem gagnagjafa gagnalíkans þegar tilgreina þarf gögn á keyrslutíma.
- Stuðningur er fyrir umbreytingu gagna Finance and Operations í tilskilda hópa. Það gerir þér kleift að sía, raða og leggja saman gögn og hengja við röklega reiknaða reiti sem eru hannaðir með formúlum sem líkjast Microsoft Excel formúlum, eins og sést á eftirfarandi myndskýringu. Frekari upplýsingar er að finna í [Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)).

[![Formúluhönnuður](./media/ER-overview-01.png)](./media/ER-overview-01.png)

Líkanavörpun sem styður rafræn skjöl á innleið hefur eftirfarandi getu:

- Hægt er að nota mismunandi uppfæranlegar gagnaeiningar sem mörk. Á meðal þessara gagnaþátta eru töflur, gagnaeiningar og yfirlit. Hægt er að uppfæra gögnin með því að nota gögnin úr rafrænum skjölum á innleið. Hægt er að nota mörg mörk í einni líkanavörpun.
- Það styður ílagsfæribreytur notanda sem má skilgreina sem gagnagjafa gagnalíkans þegar tilgreina þarf gögn á keyrslutíma.

Þáttur gagnalíkans er hannaður fyrir hvert viðskiptasvið sem nota á sem sameinaðan gagnagjafa fyrir skýrslugerð sem einangrar skýrslugerð frá efnislegri innleiðingu gagnagjafa. Hann sýnir viðskiptahugtök fyrir tiltekin svið og virkni í skjámynd sem gerir frumhönnun og frekara viðhald á skýrslugerðarsniði skilvirkara.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Sniðsþáttur fyrir rafræn skjöl á útleið

Snið er skema skýrsluúttaks sem myndast á keyrslutíma. Skema samanstendur af eftirfarandi þáttum:

- Snið sem skilgreinir skipulag og innihald í rafrænu skjali á útleið sem er myndað á keyrslutíma.
- Gagnagjafar, sem ílagsfæribreytur notanda og gagnalíkön fyrir tiltekin svið sem nota valda líkanavörpun.
- Sniðsvörpun, sem safn bindingar fyrir gagnagjafa sniða sem eru með einstakar sniðseiningar sem tilgreina, á keyrslutíma, gagnaflæði og reglur um myndun úttakssniðs.
- Villuleitarsnið, sem hópur af samskipanlegum reglum sem stýra skýrslugerð á keyrslutíma, háð samhengi keyrslu. Til dæmis gæti verið regla sem stöðvar úttaksmyndun fyrir greiðslur lánardrottins og beitir undantekningu þegar tilteknar eigindir valins lánardrottins vantar, eins og númer bankareiknings.

Þáttur sniðs styður eftirfarandi aðgerðir:

- Stofnun skýrslugerðarúttaks sem einstakar skrár í mismunandi sniði, eins og texti, XML, Microsoft Word skjal eða vinnublað.
- Stofnun margra aðgreindra skráa og einnig að steypa þessum skrám saman í ZIP-skrár.

Sniðsþáttur gerir þér kleift að hengja við tilteknar skrár sem hægt er að nota í skýrslugerðarúttaki:

- Excel-vinnubækur Sem inniheldur vinnublað sem sem má nota sem sniðmát fyrir úttak á OPENXML vinnublaðssniði;
- Word-skrár sem innihalda skjal sem nota má sem sniðmát fyrir úttak á Microsoft Word skjalasniði
- Aðrar skrár sem geta verið felldar inn í úttakssnið sem fyrirfram skilgreindar skrár.

Eftirfarandi dæmi sýnir gagnaflæðið fyrir þessi snið.

[![Gagnaflæði fyrir sniðsþætti á útleið](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Til að keyra eina sniðsskilgreiningu fyrir rafræna skýrslugerð og búa til rafrænt skjal til að senda út verður þú að auðkenna vörpun skilgreiningarsniðsins.

#### <a name="format-components-for-incoming-electronic-documents"></a>Sniðsþættir fyrir rafræn skjöl á innleið
Sniðsþáttur er skema skjals á innleið sem er flutt inn á keyrslutíma. Skema samanstendur af eftirfarandi þáttum:

- Snið sem skilgreinir skipulag og innihald rafræns skjals á innleið sem inniheldur gögn sem eru flutt inn á keyrslutíma. Sniðsþáttur er notaður til að þátta skjal á innleið á ýmis snið, eins og texta og XML.
- Sniðsvörpun sem bindur einstakar sniðseiningar í einingar í gagnalíkani fyrir tiltekin svið. Einingarnar í gagnalíkani tilgreina, á keyrslutíma, gagnaflæði og reglur fyrir innflutning gagna úr skjali á innleið og geyma svo gögnin í gagnalíkani.
- Villuleitarsnið, sem hópur af samskiptanlegum reglum sem stýra gagnainnflutningi á keyrslutíma, háð samhengi keyrslu. Til dæmis gæti verið regla sem stöðvar innflutning á gögnum bankayfirlits sem er með greiðslur lánardrottins og beitir undantekningu þegar tilteknar eigindir lánardrottins vantar, eins og auðkenniskóði lánardrottins.

Eftirfarandi dæmi sýnir gagnaflæðið fyrir þessi snið.

[![Gagnaflæði fyrir sniðsþætti á innleið](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Til að keyra eina sniðsskilgreiningu til að flytja gögn úr rafrænu skjali á innleið, verður að auðkenna tilætlaða vörpun skilgreiningarsniðsins og einnig samþættingarstað vörpunar líkans. Hægt er að nota sömu vörpun líkans og áfangastaði með mismunandi sniðum fyrir mismunandi gerðir skjala á innleið.

#### <a name="component-versioning"></a>Sögugeymni íhlutar

Sögugeymnin er studd fyrir ER þætti. Eftirfarandi verkflæði er til staðar til að stýra breytingum í þáttum rafrænnar skýrslugerðar:

1. Útgáfan sem var upphaflega stofnuð er merkt sem **Drög**. Útgáfan er hægt að breyta og er tiltæk fyrir prófunarkeyrslu.
2. Útgáfunni **Drög** má breyta í útgáfuna **Lokið**. Hægt er að nota þessa útgáfu í staðbundna skýrslugerðarferli.
3. Útgáfunni **Lokið** má breyta í útgáfuna **Samnýtt**. Útgáfan er birt á LCS og hægt er að nota í altæku skýrslugerðarferli.
4. Útgáfunni **Samnýtt** má breyta í útgáfuna **Hætt við**. Síðan er hægt að eyða þessari útgáfu.

Útgáfur sem hafa stöðuna **Lokið** eða **Samnýtt** eru tiltækar fyrir önnur gagnaskipti. Hægt er að framkvæma eftirfarandi aðgerðir á þætti sem hefur þessar stöður:

- Þætti má raða í XML-snið og flytja út sem skrá á XML-sniði.
- Hægt er að endurraða þættinum úr XML-skrá og flytja inn í Finance and Operations sem nýja útgáfu ER-þáttar.

#### <a name="component-date-effectivity"></a>Dagsetning á virkni íhlutar

ER þáttarútgáfur eru virkar eftir dagsetningum. Hægt er að stilla dagsetninguna **Virkt frá** fyrir þátt rafrænnar skýrslugerðar þannig að hún tilgreini þá dagsetningu sem þátturinn verður virkur fyrir skýrsluferla. Finance and Operations lotudagsetning er notuð til að skilgreina hvort þáttur er gildur fyrir framkvæmd. Nýjusta útgáfa er notuð fyrir skýrsluferli þegar fleiri en ein útgáfa er í gildi fyrir tiltekna dagsetningu.

#### <a name="component-access"></a>Aðgangur að þáttum

Aðgangur ER sniðþátta fer eftir ISO-lands-/ svæðiskóða stillingum. Þegar þessi stilling er auð fyrir valda útgáfu skilgreiningar sniðs, er hægt að nálgast sniðsþátt úr hvaða fyrirtæki sem er á keyrslutíma. Þegar þessi stilling inniheldur ISO lands-/ svæðiskóða, er sniðsþáttur tiltækur eingöngu frá fyrirtækjum þar sem aðalaðsetur er tilgreint fyrir einn sniðsþátt ISO lands-/svæðiskóða.

Mismunandi útgáfur af gagnasniðsþáttum mega vera með mismunandi stillingar ISO lands-/ svæðiskóða.

#### <a name="configuration"></a>Stilling

Skilgreining rafrænnar skýrslugerðar er pökkun tiltekins þáttar í rafrænni skýrslugerð. Sá þáttur getur annaðhvort verið gagnalíkansþáttur eða sniðsþáttur. Stilling getur innihaldið mismunandi útgáfur þáttar rafrænnar skýrslugerðar. Hver stilling er merkt sem eign tiltekinnar stillingarveitu. Hægt er að breyta **Drög** útgáfu þáttar í stillingu þegar eigandi stillingarinnar hefur verið valinn sem virkur veitandi í stillingum rafrænnar skýrslugerðar í Finance and Operations.

Hver líkanaskilgreining inniheldur gagnalíkansþátt. Ný skilgreining sniðs getur komið frá tiltekinni skilgreiningu gagnalíkans. Í stillingatrénu birtist skilgreining sem er stofnuð sem undirliður upphaflegrar gagnalíkansstillingar.

Sniðsskilgreining sem er stofnuð inniheldur sniðsþátt. Gagnalíkansþáttur upphaflegrar stillingar líkans er sjálfkrafa settur inn í sniðsþátt undirliðsstillingar sem sjálfgefinn gagnagjafi.

Skilgreining ER er samnýtt fyrir fyrirtæki í Finance and Operations.

#### <a name="provider"></a>Veita

ER-veitan er auðkenni aðila sem er notuð til að tilgreina höfund (eiganda) fyrir hverja ER-skilgreiningu. ER leyfir þér að að stjórna lista yfir veitendur skilgreininga. Skilgreiningarsnið sem eru gefin út fyrir rafrænt skjal sem hluti af lausn Finance and Operations eru merktar sem í eigu **Microsoft** skilgreiningarveitu.

Til að fræðast um hvernig á að skrá nýja þjónustuveitu rafrænnar skýrslugerðar skaltu spila verkleiðbeiningarnar **Stofna veitanda skilgreiningar í rafrænni skýrslugerð og merkja sem virkan** (hluti af viðskiptaferlinu **7.5.4.3 Komast yfir/þróa þætti fyrir upplýsingatækniþjónustu/lausnir (10677)**).

#### <a name="repository"></a>Geymsla

ER-gagnasafn vistar ER-skilgreiningar. Fjórar gerðir af ER-gagnasöfnum eru studdar sem stendur: **Rekstrartilföng**, **LCS-verk (LCS)**, **Skráakerfi** og **Skilgreiningarþjónusta reglugerðar (RCS)**.

Gagnasafnið **Rekstrartilföng** veitir aðgang að lista skilgreininga sem Microsoft, sem veitandi skilgreininga í rafrænni skýrslugerð, gefur út sem hluta af Finance and Operations lausninni. Þessar stillingar er hægt að flytja inn í núverandi Finance and Operations tilvik og nota fyrir rafræna skýrslugerð. Einnig er hægt að nota þær fyrir frekari staðfæringar og sérstillingar.

**LCS-verks** gagnasafn veitir aðgang að lista yfir skilgreiningar ákveðins LCS-verks (eignasafn LCS-verks) sem var valið á skráningarstigi gagnasafns. Rafræn skýrslugerð gerir þér kleift að hlaða upp samnýttum skilgreiningum úr núverandi tilviki í Finance and Operations í tiltekna geymslu fyrir **LCS-verk** . Þú getur einnig flutt inn stillingar úr geymslu fyrir **LCS-verk** í núverandi tilvik Finance and Operations.

Gagnasafn **Skráakerfis** veitir aðgang að lista yfir skilgreiningar sem eru staðsettar sem xml-skrár í tiltekinni möppu í staðbundnu skráakerfi vélarinnar þar sem AOS-þjónustan er hýst. Nauðsynleg mappa er valin á skráningarstigi gagnasafns. Hægt er að flytja inn skilgreiningar úr gagnasafni **Skráakerfis** í núverandi tilviki Finance and Operations. Athugið að þessi gagnasafnsgerð er aðgengileg í eftirfarandi umhverfi Dynamics 365 for Finance and Operations:
- umhverfi í skýi sett upp í þróunarlegum tilgangi (inniheldur prufulíkön úr inniföldum pökkum)
- staðbundið uppsett umhverfi (á staðnum eða uppsetning staðbundinna viðskiptagagna (LBD))

Farið á síðuna [Stillingar fyrir innflutning rafrænnar skýrslugerðar (ER)](/electronic-reporting-import-ger-configurations.md) til að fá frekari upplýsingar um þetta.

Gagnasafn **RCS-tilviks** veitir aðgang að lista yfir skilgreiningar á tilteknu RCS-tilviki sem var valið á skráningarstigi gagnasafns. Rafræn skýrslugerð gerir þér kleift að flytja inn skilgreiningar, sem er lokið eða eru samnýttar, úr völdu RCS-tilviki í núgildandi tilvik Finance and Operations og notaðar í rafrænni skýrslugerð.

Farið á síðuna [Stillingar fyrir innflutning rafrænnar skýrslugerðar (ER) úr skilgreiningarþjónustu reglugerðar (RCS)](/rcs-download-configurations.md) til að fá frekari upplýsingar um þetta.

Hægt er að skrá nauðsynleg gagnasöfn **LCS-verks**, **Skráakerfis** og **Skilgreiningarþjónustu reglugerðar (RCS)**, hvert safn fyrir sig, fyrir hverja skilgreiningarveitu fyrir núgildandi tilvik Finance and Operations. Hvert gagnasafn getur verið sérmerkt tiltekinni skilgreiningarveitu.

## <a name="supported-scenarios"></a>Studdar aðstæður
### <a name="building-a-data-model"></a>Byggja gagnalíkan

ER býður upp á hönnun líkana sem má nota til að byggja gagnalíkan fyrir tiltekin viðskiptasvið. Allir umdæmissértækir viðskiptaaðilar og tengsl milli þeirra er hægt að sýna í gagnalíkani sem stigskipt uppbygging.  Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð gagnalíkans (gagnalíkan á sviði greiðslu)

[![Gagnalíkan fyrir greiðslusvæði](./media/ER-overview-04.png)](./media/ER-overview-04.png)

til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER hönnun gagnalíkan fyrir sértækt svið** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="translating-data-model-content"></a>Þýðing á innihaldi gagnalíkans

Hægt er að þýða innihald gagnalíkans (merki og lýsingar) yfir á önnur tungumál sem Finance and Operations styður. Gott væri að þýða innihald gagnalíkans af eftirfarandi ástæðum:

- Til að gera það skiljanlegra á hönnunartíma fyrir sniðhönnuði sem tala önnur tungumál og nota gagnalíkanið fyrir gagnavörpun sniðsþátta.
- Til að gera innihaldið notendavænna á keyrslutíma, með því að birta tilkynningar og hjálp fyrir færibreytur á keyrslutíma og skilgreind villuleitarskilaboð (villur og viðvaranir) á því tungumáli sem innskráður notandi kýs.

Eftirfarandi skýringarmynd sýnir dæmi þar sem innihald gagnalíkans er þýtt af ensku yfir á japönsku.

[![Innihald gagnalíkans á ensku](./media/ER-overview-05.png)](./media/ER-overview-05.png)

[![Innihald gagnalíkans þýtt yfir á japönsku](./media/ER-overview-06.png)](./media/ER-overview-06.png)

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Stilling gagna í líkanavörpunum fyrir skjöl á útleið

Rafræn skýrslugerð hefur að geyma vörpunarhönnun sem leyfir notendum að varpa gagnalíkönum sem þeir hafa hannað í tiltekna gagnagjafa Finance and Operations. Gögnin verða flutt inn samkvæmt vörpuninni á keyrslutíma úr völdum gagnagjöfum í gagnalíkanið. Gagnalíkanið er svo notað sem útdráttargagnagjafi allra sniða í rafrænni skýrslugerð sem búa til rafræn skjöl á útleið. Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð af vörpun gagnalíkans (**SEPA kreditfærsla** líkanavörpun fyrir gagnalíkan á sviði greiðslu)

[![Dæmi um gagnalíkansvörpun](./media/ER-overview-07.png)](./media/ER-overview-07.png)

Spila **ER Skilgreining líkanavörpunar og velja gagnagjafa** og **ER vörpun gagnalíkans í valda gagnagjafa** verkleiðbeiningar (hluti af **7.5.4.3 Acquire/Develop IT þjónustu-/lausnaþættir (10677)** viðskiptaferli) til að kynna þér aðstæðurnar í smáatriðum.

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Stilling gagna í líkanavörpunum fyrir skjöl á innleið
Rafræn skýrslugerð hefur að geyma hönnun líkanavörpunar sem leyfir notendum að varpa gagnalíkönum sem þeir hafa hannað á tiltekna staði. Til dæmis er hægt að varpa gagnalíkönum í uppfæranlega gagnaþætti Finance and Operations (töflur, gagnaeiningar og yfirlit). Gögnin í Finance and Operations verða uppfærð samkvæmt vörpuninni á keyrslutíma með því að nota gögnin úr gagnalíkaninu. Gagnalíkanið er útdráttargeymsla fyrir snið í rafrænni skýrslugerð og er því fullt af gögnum sem eru flutt inn úr rafrænum skjölum á innleið. Eftirfarandi skýringarmynd sýnir dæmi um þessa gerð gagnalíkansvörpunar. Í þessu dæmi er vörpunin á gagnalíkani fyrir greiðslusvæði **Innflutningsvörpun fyrir NETS** notuð til að styðja við innflutning á bankayfirlitum á NETS-bankasniði fyrir Noreg.

[![Dæmi um innflutningsvörpun fyrir NETS gagnalíkan](./media/ER-overview-08.png)](./media/ER-overview-08.png)

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Geyma hannaðan þátt líkans sem líkanastillingu

Rafræn skýrslugerð getur geymt hannað gagnalíkan, ásamt tengdum gagnavörpunum, sem gagnastilling á núverandi tilviki Finance and Operations. Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð skilgreiningar gagnalíkans (skilgreining líkans fyrir greiðslu)

Spila **ER Skilgreining líkanavörpunar til að velja gagnagjafa** verkleiðbeiningar (hluti af **7.5.4.3 Acquire/Develop IT þjónustu-/lausnaþættir (10677)** viðskiptaferli) til að kynna þér aðstæðurnar í smáatriðum.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Byggja snið sem notar gagnalíkan sem grunneiningu

Rafræn skýrslugerð styður sniðshönnun sem þú getur notað til að setja upp snið fyrir rafrænt skjal fyrir valið viðskiptasvæði með því að velja líkansþáttinn sem grunn. Sama sniðshönnun í rafrænni skýrslugerð býður upp á möguleika á að varpa stofnuðu sniði á valið gagnalíkanavörpunarsvæði sem gagnagjafa. Eftirfarandi skýringarmynd sýnir dæmi um slíka gerð sniðs (skilgreiningarsniðið sem styður í **BACS** greiðslusnið fyrir Bretland).

[![Dæmi um snið sem hefur gagnalíkan sem grunn](./media/ER-overview-09.png)](./media/ER-overview-09.png)

Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER hönnun sniðs fyrir sértækt svið** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Byggja skilgreiningu til að mynda rafræn skjöl í OPENXML sniði vinnublaðs

Hægt er að nota sniðshönnun fyrir rafræna skýrslugerð til að búa til rafræn skjöl á vinnublaðssniðinu OPENXML. Eftirfarandi skýringarmynd sýnir dæmi um slíka gerð sniðs (skilgreining sniðs til að mynda OPENXML vinnublað með upplýsingum um valda greiðslubók).

[![Pic-ER-format-Excel](./media/ER-overview-10.png)](./media/ER-overview-10.png)

Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER stofna skilgreiningu fyrir skýrslur í OPENXML-sniði** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) . Notaðu Excel-skrána [Sniðmát fyrir greiðsluskýrslu (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202) sem sniðmát, sem hluta af verkefnaleiðbeiningunum við að flytja inn snið.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Að búa til stillingu til að mynda rafræn skjöl á Word-skjalssniðinu.
Hægt er að nota sniðshönnun fyrir rafræna skýrslugerð til að búa til rafræn skjöl á skjalssniði fyrir Word. Eftirfarandi skýringarmynd sýnir dæmi um þessa gerð sniðs. Athugaðu að þetta snið notar aftur fyrirliggjandi grunnstillingu fyrir rafræna skýrslugerð sem var upphaflega hönnuð til að búa til skýrsluúttakið á OPENXML-sniði.

[![Pic-ER-format-Word](./media/ER-overview-11.png)](./media/ER-overview-11.png)

Til að kynna þér aðstæðurnar í smáatriðum skaltu spila verkleiðbeiningarnar Rafræn skýrslugerð - Hannaðu stillingu til að búa til skýrslur á Microsoft Word-sniðinu (hluti af viðskiptaferlinu 7.5.4.3 Komast yfir/þróa þætti fyrir upplýsingatækniþjónustu/lausnir (10677)). Notaðu eftirfarandi Word-skrár sem sniðmát fyrir snið rafrænnar skýrslugerðar, sem hluta af verkleiðbeiningunum fyrir innflutning á sniðmáti.

- [Sniðmát greiðsluskýrslu (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Afmarkað sniðmát greiðsluskýrslu (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Að búa til stillingu til að flytja inn gögn úr rafrænum skjölum á innleið
Hægt er að nota sniðshönnun í rafrænni skýrslugerð til að lýsa rafrænu skjali sem er hugsað fyrir gagnainnflutning á annaðhvort XML eða textasniði. Hannaða sniðið er notað til að þátta skjal á innleið. Hægt er að nota vörpunarhönnun fyrir snið í rafrænni skýrslugerð til að skilgreina bindingu eininga hannaðs sniðs við gagnalíkanið. Eftirfarandi skýringarmyndir sýna dæmi um þessa gerð sniðs og sniðsvörpunar. Í þessu dæmi eru NETS bankayfirlit sem innihalda upplýsingar um greiðslu lánardrottna á textasniði flutt inn.

[![Sniðshönnun í rafrænni skýrslugerð](./media/ER-overview-12.png)](./media/ER-overview-12.png)

[![Hönnun fyrir vörpun gagnalíkans í rafrænni skýrslugerð](./media/ER-overview-13.png)](./media/ER-overview-13.png)

Til að kynna þér aðstæðurnar í smáatriðum skaltu spila verkleiðbeiningarnar Stofnaðu nauðsynlegar stillingar í rafrænni skýrslugerð til að flytja inn gögn úr utanaðkomandi skrá (hluti af viðskiptaferlinu 7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)). Notaðu eftirfarandi skrár til að spila þessar leiðbeiningar:

- [Stilling á gagnalíkani í rafrænni skýrslugerð (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Sniðsskilgreining í rafrænni skýrslugerð (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Sýnishorn af skjali á innleið á XML-sniði (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Sýnishorn af vinnubók til að stýra gögnum skjala á innleið (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Geyma hannaðan sniðsþátt í skilgreiningarsniði

Rafræn skýrslugerð getur geymt hannað snið með skilgreindum gagnavörpunum sem sniðsskilgreiningu fyrir núverandi tilvik Finance and Operations. Fyrrgreint sýnidæmi sýnir dæmi af þessari gerð skilgreiningarsniðs (**BACS (UK)**, sem er undireining á **greiðslulíkan** skilgreiningu). Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER hönnun sniðs fyrir sértækt svið** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="configuring-finance-and-operations-to-start-to-use-a-created-format-internally"></a>Stilling Finance and Operations til að byrja að nota stofnað snið innanhúss

Hægt er að stilla Finance and Operations til að byrja að nota stofnað snið fyrir rafræna skýrslumyndun. Tilvísun í stofnaða stillingarsniðið ætti að skilgreina í stillingum tiltekins sviðs. Til dæmis til að byrja að nota sniðskilgreiningu Rafræn skýrslugerð fyrir rafrænar greiðslur lánadrottins á BACS sniði, ætti að vera vísað í skilgreiningarsniðið í tilteknum greiðslumátum, eins og sýnt er í eftirfarandi skýringamyndir:

[![BACS (UK) sniðsskilgreining](./media/ER-overview-14.png)](./media/ER-overview-14.png)

[![Vísað í sniðið BACS (UK) í greiðslumáta](./media/ER-overview-15.png)](./media/ER-overview-15.png)

Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Er nota snið til að mynda rafrænt skjal fyrir greiðslur** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

## <a name="handling-er-components"></a>Meðhöndlun ER þátta
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Birting ER þátta í LCS til að bjóða það út á við (staðfærsla)

Eigandi þáttar (líkan eða snið) sem hefur verið stofnað getur notað ER til að birta kláraða útgáfu þáttarins í LCS. Geymsla **LCS verks** fyrir gildandi ER stillingaveitu er krafist. Þegar staða fullunnar útgáfu þáttar er breytt úr **LOKIÐ** í **SAMNÝTT**, er útgáfan er birt í LCS. Þegar þáttur hefur verið birtur í LCS verður eigandi þess þáttar veitandi þjónustu til að styðja þennan þátt. T.d. ef þessi sniðsþáttur er hannaður til að búa til rafrænt skjal sem er krafist samkvæmt lögum (t.d. í samræmi við staðfærsluaðstæður), gerir þessi þjónusta ráð fyrir að halda sniðinu í samræmi við lögboðnar breytingar og hönnuðurinn muni gefa út nýjar útgáfur þegar styðja þarf nýjar lögbundnar kröfur. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Er hlaða upp skilgreiningu í Lifecycle Services** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Flytja þátt ER úr LCS til nota innan kerfis

Rafræn skýrslugerð gerir það mögulegt að flytja inn þætti rafrænnar skýrslugerðar úr LCS í núverandi tilvik Finance and Operations. Geymslu af gerðinni **LCS verki** er krafist. Þegar rafrænn skýrsluþáttur hefur verið fluttur inn úr LCS í núverandi tilvik Finance and Operations, verður eigandi tilviksins neytandi þjónustunnar sem eigandi (höfundur) innflutta þáttarins veitir. Ef til dæmis sniðsþáttur er hannaður til að mynda tiltekið rafrænt skjal úr Finance and Operations á sniði sem er sértækt fyrir land/svæði (staðfærsluaðstæður), gerir notkun þessarar þjónustu ráð fyrir því að neytandi þjónustunnar geti fengið allar uppfærslur sem eru gerðar á því sniði, til að það sé áfram í samræmi við lögboðnar kröfur. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Flytja inn skilgreiningu úr Lifecycle Services** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Byggja snið og velja annað snið sem grunn (sérsnið).

ER gerir þér kleift að stofna (leita út) nýjan þátt úr gildandi útgáfu af þætti (grunni) sem var flutt úr LCS. Til dæmis, notandi vill afleiða nýja snið sem á að innleiða sérstakar þarfir fyrir rafrænt skjal (til dæmis viðbótarreit eða yfirgripsmikla lýsing) til að styðja aðstæður sérsníðingar. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Uppfæra snið með innleiðingu nýs grunns fyrir það** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Uppfæra snið því að velja nýja útgáfu af grunnsniði (endurreikna grunn)

ER leyfir þér að taka sjálfkrafa í gagn breytingar á nýjustu útgáfu af þættinum grunngögn í gildandi drögum af afleiddum þætti. Þetta ferli kallast *endurreikningur*. Til dæmis, geta nýjar breytingar á reglum sem voru kynntar í síðastu útgáfu sniðsþáttar sem var flutt úr LCS verið sjálfkrafa sameinaðar við í sérsniðna útgáfu af þessu sniði rafrænna skjala. Allar breytingar sem ekki er hægt að sameina sjálfvirkt eru taldar árekstrar. Þessir árekstrar eru ætlaðir fyrir handvirka úrlausn í hönnunartæki fyrir viðkomandi þátt. Til að kynna þér aðstæðurnar í smáatriðum skaltu spila verkleiðbeiningarnar **ER Uppfæra snið með innleiðingu nýs grunns af því sniði** (hluti af **7.5.5.3 Komast yfir/þróa íhluti fyrir breytta upplýsingatækniþjónustu/lausnir (10683)** viðskiptaferli).

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-and-operations-solution"></a>Listi yfir skilgreiningar rafrænnar skýrslugerðar sem eru í Finance and Operations lausninni

| Skilgreiningar gagnalíkana tengd ákveðnum lénum: Titill | Lén                | Gagnalíkan – háð skilgreiningarsnið: Titill | Lýsing                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Líkan endurskoðunarskrár                                 | Endurskoðun       |                                                   |                                                                    |
|                                                  |                       | Endurskoðunarskrá (NL)                                   | endurskoðunarskrársnið fyrir Holland                                  |
| BAS-líkan                                        | skattaskýrslugerð         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | BAS-snið fyrir Ástralíu                                           |
| Líkan skema fyrir byggingariðnað               | skattaskýrslugerð         |                                                   |                                                                    |
|                                                  |                       | CIS mánaðarleg ávöxtun (UK)                           | CIS snið fyrir mánaðarlega ávöxtun fyrir Bretland                   |
| líkan innheimtubréfs                          | Rafræn reikningsfærsla  |                                                   |                                                                    |
|                                                  |                       | OIOUBL innheimtubréf (DK)                     | OIOUBL snið innheimtubréfs fyrir Danmörku                        |
| Rafrænt reikningshaldslíkan (MX)          | skattaskýrslugerð         |                                                   |                                                                    |
|                                                  |                       | Aukafjárhagur XML (MX)                         | Viðbótar fjárhagsfærslur eftir skýrslusniði lykils fyrir Mexíkó |
|                                                  |                       | Bókhaldslykill XML (MX)                         | skýrslusnið bókhaldslykils fyrir Mexíkó                          |
|                                                  |                       | Færslubækur XML (MX)                                 | Skýrslusnið færslubókarfærsla fyrir Mexíkó                      |
|                                                  |                       | Prófjöfnuður XML (MX)                            | Skýrslusniðið prófjöfnuðar fyrir Mexíkó                             |
| Elster-líkan                                     | skattaskýrslugerð         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Elster-Snið fyrir Þýskaland                                          |
| Líkan ESB-sölulista                              | Viðskiptaskýrslugjöf       |                                                   |                                                                    |
|                                                  |                       |  ESB-sölulisti (DE)                                | ESB-sölulisti - TXT-snið fyrir Þýskaland                               |
|                                                  |                       | ESB-sölulista (DK)                                | ESB-sölulisti - TXT-snið fyrir Danmörk                               |
|                                                  |                       |  ESB-sölulisti (FR)                                | ESB-sölulisti - XML-snið fyrir frakkland                                |
|                                                  |                       | ESB-sölulista (NL)                                | ESB-sölulisti - XML-snið fyrir Holland                           |
|                                                  |                       | ESB-sölulista TXT (Bretland)                            | ESB-sölulisti - TXT-snið fyrir Bretland                    |
|                                                  |                       | ESB-sölulisti - XML (UK)                            | ESB-sölulisti - XML-snið fyrir Bretland                    |
|                                                  |                       | ESB-sölulista eftir dálkaskýrslu                   | ESB-sölulista eftir dálkaskýrslu                                    |
|                                                  |                       | ESB-sölulisti eftir línum skýrsla                      | ESB-sölulisti eftir línum skýrsla                                       |
| FEC reikningshaldslíkan (FR)                        | skattaskýrslugerð         |                                                   |                                                                    |
|                                                  |                       | FEC-bókhaldsgagna XML (FR)                      | Útflutningur FEC-bókhaldsgagna - XML-snið fyrir frakkland                   |
| Þýska endurskoðunarskrá                                | Endurskoðun       |                                                   |                                                                    |
|                                                  |                       | Þýskt úttak endurskoðunarskrár                          | Úttak endurskoðunarskrár fyrir Þýskaland og Austurríki.                          |
| Intrastat-líkan                                  | Viðskiptaskýrslugjöf       |                                                   |                                                                    |
|                                                  |                       | Intrastat-(DE)                                    | Intrastat-snið fyrir Þýskaland                                       |
|                                                  |                       | Intrastat-(DK)                                    | Intrastat-snið fyrir Danmörk                                       |
|                                                  |                       | Intrastat-INTRACOM (FR)                           | Intrastat-INTRACOM snið fyrir Frakkland                               |
|                                                  |                       | Intrastat-SAISUNIC (FR)                           | Intrastat-SAISUNIC snið fyrir Frakkland                               |
|                                                  |                       | Intrastat-(NL)                                    | Intrastat-snið fyrir Holland                               |
|                                                  |                       | Intrastat-(Bretland)                                    | Intrastat-snið fyrir BRETLANDI                            |
|                                                  |                       | Intrastat-skýrsla                                  | Intrastat-Excel eftirlitsskýrsla                                     |
| Líkan Reiknings viðskiptavinar                           | Rafræn reikningsfærsla  |                                                   |                                                                    |
|                                                  |                       | OIOUBL kreditnóta verks (DK)                   | OIOUBL Kreditnóta verkefnis-snið fyrir Danmörk                      |
|                                                  |                       | OIOUBL Verkreikningur (DK)                       | OIOUBL verkreikningur-snið fyrir Danmörk                          |
|                                                  |                       | OIOUBL Sölukreditnóta (DK)                     | OIOUBL snið sölukreditnótu fyrir Danmörku                        |
|                                                  |                       | OIOUBL sölureikningur (DK)                         | OIOUBL snið sölureiknings fyrir danmörku                            |
| OB Skattframtalslíkan                             | skattaskýrslugerð         |                                                   |                                                                    |
|                                                  |                       | OB skattframtal (NL)                               | OB snið skattframtals fyrir Holland                          |
| Greiðslulíkan                                    | Greiðslur              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Betalingsservice greiðslusnið fyrir Danmörku                        |
|                                                  |                       | Greiðsla á víxli (FR)                  | Snið fyrir Greiðsla á víxli fyrir frakkland                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91 greiðslusnið fyrir holland                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB greiðslusnið fyrir beint debet fyrir frakkland                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB snið fyrir greiðsla lánardrottins innanlands fyrir frakkland.                    |
|                                                  |                       | Nordea lánardrottinn (DK)                                | Greiðslusnið lánardrottins Nordea netbanka fyrir danmörku         |
|                                                  |                       |  ANZ þjónusta beins kredits (AU)                    | Snið fyrir ANZ þjónustu beins kredits fyrir Ástralíu                 |
|                                                  |                       | CBA þjónusta beins kredits (AU)                    | Snið fyrir CBA þjónustu beins kredits fyrir Ástralíu                 |
|                                                  |                       | NAB þjónusta beins kredits (AU)                    | Snið fyrir NAB þjónustu beins kredits fyrir Ástralíu                 |
|                                                  |                       | STG þjónusta beins kredits (AU)                    | Snið fyrir STG þjónustu beins kredits fyrir Ástralíu                 |
|                                                  |                       | WBC kerfi fyrir beina færslu (AU)                      | Snið fyrir WBC kerfi fyrir beina færslu fyrir Ástralíu                   |
|                                                  |                       | DirectLink (NZ)                                   | Snið fyrir DirectLink fyrir Nýja-Sjáland                              |
|                                                  |                       | JBA greiðsluskrá (JP)                             | JBA greiðslusnið fyrir Japan                                       |
|                                                  |                       | ISO20022-kreditfærsla                          | SEPA-kreditfærsla snið fyrir Evrópu                             |
|                                                  |                       | ISO20022-kreditfærsla (FR)                     | SEPA snið kreditfærslu fyrir Frakkland                             |
|                                                  |                       | ISO20022-kreditfærsla (DE)                     | SEPA snið kreditfærslu fyrir Þýskaland                            |
|                                                  |                       | ISO20022-kreditfærsla (NL)                     | SEPA snið kreditfærslu fyrir Holland                    |
|                                                  |                       | ISO20022-beingreiðsla                             | SEPA-snið beingreiðslu fyrir Evrópu                                |
|                                                  |                       | ISO20022-beingreiðsla (FR)                        | SEPA snið fyrir beingreiðslu fyrir Evrópu                                |
|                                                  |                       | ISO20022-beingreiðsla (DE)                        | SEPA snið fyrir beingreiðslu fyrir Þýskaland                               |
|                                                  |                       | ISO20022-beingreiðsla (NL)                        | SEPA snið fyrir beingreiðslu fyrir Fyrir Holland                       |
|                                                  |                       | BACS (UK)                                         | BACS snið greiðsla lánardrottins fyrir Bretland                  |
| Bakfærð gjöld                                   | skattaskýrslugerð         |                                                   |                                                                    |
|                                                  |                       | Sölulisti bakfærðra gjalda                         | Snið Sölulista bakfærðra gjalda                                   |
| Hollensk XBRL Samþættingarstilling                     | XBRL skýrslugerð        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Semansys XBRL útflutningssnið fyrir holland.                    |
| GAF líkan (MY)                                   | Endurskoðun       |                                                   |                                                                    |
|                                                  |                       | GAF skrá (MY)                                     | Snið GAF fyrir Malasía                                         |
| Aldursgreiningarskýrsla lánardrottins (CN)                         | Greining gagna lánardrottins |                                                   |                                                                    |
|                                                  |                       | Snið Aldursskýrslu lánardrottins (CN)                   | Snið Aldursskýrslu lánardrottins fyrir Kína                               |
| líkan um verktakamiða lánardrottins                 | Greining gagna lánardrottins |                                                   |                                                                    |
|                                                  |                       | Verktakamiðar lánardrottins (IS)                   | Verktakamiðar lánardrottins fyrir Ísland                      |
|                                                  |                       | Skýrsla um verktakamiða lánardrottins (IS)            | Skýrsla um verktakamiða lánardrottins fyrir Ísland                      |

## <a name="additional-resources"></a>Frekari upplýsingar

[Kröfur um staðfæringu - stofna Skilgreining fyrir rafræna skýrslugerð](electronic-reporting-configuration.md)

[Stjórnun á lífsferli fyrir stillingar Rafrænnar skýrslugerðar](general-electronic-reporting-manage-configuration-lifecycle.md)

