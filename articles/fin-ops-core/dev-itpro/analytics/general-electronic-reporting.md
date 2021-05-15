---
title: Yfirlit yfir rafræna skýrslugerð (ER)
description: Í þessari grein er að finna yfirlit yfir verkfærið „Rafræn skýrslugerð“. Þar er lýst lykilhugtökum, studddum aðstæður og sniðum sem eru hluti af lausninni.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26088a01b0e849a5df559631591ec65d7885452b
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944366"
---
# <a name="electronic-reporting-er-overview"></a>Yfirlit yfir rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna yfirlit yfir verkfærið „Rafræn skýrslugerð“. Þar á meðal er að finna upplýsingar um lykilhugtök, sviðsmyndir sem Rafræn skýrslugerð styður og lista yfir snið sem hafa verið hönnuð og gefin út sem hluti af lausninni.

Rafræn skýrslugerð (ER) er verkfæri sem hægt er að nota til að skilgreina sniðið á rafrænum skjölum á innleið og útleið í samræmi við ákvæði laga mismunandi landa/svæða. ER (rafræn skýrslugerð) gerir þér kleift að stjórna þessum sniðum í lífsferli þeirra. Til dæmis er hægt að taka upp nýjar lagalegar kröfur, og búa til viðskiptaskjöl á tilskildu sniði til að skiptast rafrænt á upplýsingum við stjórnvöld, banka og fleiri aðila.

Vélar fyrir rafræna skýrslugerð eru ætlaðar fyrir viðskiptanotendur í stað þróara. Þar sem þú skilgreinir snið en ekki kóða eru ferlin við að stofna og stilla snið fyrir rafræn skjöl hraðvirkari og auðveldari.

Á þessum tíma styður ER TEXT, XML Microsoft Word skjöl, og OPENXML snið vinnublaða. Hins vegar veitir viðbótarviðmót stuðning við fleiri snið.

## <a name="capabilities"></a>Geta

ER-vélin hefur eftirfarandi getu:

- Það er eitt deilt verkfæri til rafrænnar skýrslugerðar á mismunandi lénum, og kemur í stað 20 mismunandi véla sem gera einhvers konar rafræna skýrslugerð fyrir Finance and Operations.
- Það gerir snið á skýrslu einangrað úr núgildandi innleiðingu. Með öðrum orðum, snið gildir fyrir mismunandi útgáfur.
- Hann styður stofnun sérsniðinnar sniða sem byggð er á upprunalegu sniði. Það felur einnig í sér getu til að uppfæra sjálfkrafa sérhönnuð snið þegar breytingar á upprunalegu sniði eiga sér stað, vegna krafna um staðfærslu/sérsnið.
- Verður það aðal viðtekna verkfærið til að styða við kröfur um staðfæringu í rafrænni skýrslugerð – bæði fyrir Microsoft sem og microsoft samstarfsaðila;
- Það styður getu til að dreifa sniðum til viðskiptaaðila og viðskiptavini með Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Lykilhugtök

### <a name="components"></a>Íhlutir

ER styður tvær gerðir íhluta **gagnalíkan** og **Snið**.

#### <a name="data-model-and-model-mapping-components"></a>Gagnalíkan og íhlutir líkanavörpunar

Þáttur gagnalíkans er óhlutbundin framsetning á gagnaskipulagi. Hann er notaður til að lýsa tilteknu viðskiptasviði með nægilegum upplýsingum til að tilkynningaskylda fyrir það svið sé uppfyllt. Íhlutir gagnalíkans samanstendur af eftirfarandi hluta:

- <a name="DataModelComponent"></a>Gagnalíkan sem hópur af viðskiptaeiningum fyrir tiltekin svið auk stigskiptra tengslaskilgreininga á milli þessara eininga.
- <a name="ModelMappingComponent"></a>líkanavörpun sem tengir völdum gagnagjöfum forrits við einstakar einingar gagnalíkans sem tilgreinir, við keyrslutíma, gagnaflæði og reglur viðskiptagagna við þætti gagnalíkans.

Viðskiptaeining gagnalíkans er birt sem geymir (skýrsla). Eiginleikar viðskiptaeininga eru sýndir sem gagnaatriði (svæði). Hvert gagnaatriði hefur einstakt heiti, merki, lýsingu og gildi. Hægt er að hanna virði hvers atriðis svo það sé viðurkennt sem strengur, heiltala, raunverulegt, dagsetning, tölusett, Boole-gildi o.s.frv. Þar að auki getur það verið önnur færsla eða færslulisti.

Einstakur þáttur gagnalíkans getur innihaldið mörg stigveldi sviða sem eru tilgreind eftir viðskiptaeiningum. Einnig getur hann innihaldið líkanavarpanir sem styðja skýrslutengt gagnaflæði á keyrslutíma. Stigveldin verða aðgreind eftir einni færslu sem hefur verið valin sem rót líkanavörpunar. Til dæmis, Gagnalíkan fyrir greiðslusvið gæti stutt eftirfarandi varpanir:

- Fyrirtæki \> Lánardrottinn \> Greiðslufærslur AP-sviðs
- Viðskiptavinur \> Fyrirtæki \> Greiðslufærslur AR-sviðs

Athugið að viðskiptaeiningar, eins og fyrirtæki og greiðslufærslur, eru búnar til einu sinni. Mismunandi varpanir endurnota þær svo.

Líkanavörpun sem styður rafræn skjöl á útleið hefur eftirfarandi getu:

- Hægt er að nota mismunandi gagnagerðir sem gagnagjafa fyrir gagnalíkan. Til dæmis getur það notað töflur, gagnaeiningar, aðferðir eða upptalningar.
- Það styður ílagsfæribreytur notanda sem má skilgreina sem gagnagjafa gagnalíkans þegar tilgreina þarf gögn á keyrslutíma.
- Stuðningur er fyrir umbreytingu gagna í tilskilda hópa. Það leyfir þér einnig að sía, raða og leggja saman gögn og skeyta við rökrétta útreiknaða reiti sem eru hannaðir með formúlum sem líkjast Microsoft Excel-formúlum. Frekari upplýsingar er að finna í [Formúluhönnuður í rafrænni skýrslugerð (ER)](general-electronic-reporting-formula-designer.md)).

Líkanavörpun sem styður rafræn skjöl á innleið hefur eftirfarandi getu:

- Hægt er að nota mismunandi uppfæranlegar gagnaeiningar sem mörk. Á meðal þessara gagnaþátta eru töflur, gagnaeiningar og yfirlit. Hægt er að uppfæra gögnin með því að nota gögnin úr rafrænum skjölum á innleið. Hægt er að nota mörg mörk í einni líkanavörpun.
- Það styður ílagsfæribreytur notanda sem má skilgreina sem gagnagjafa gagnalíkans þegar tilgreina þarf gögn á keyrslutíma.

Þáttur gagnalíkans er hannaður fyrir hvert viðskiptasvið sem nota á sem sameinaðan gagnagjafa fyrir skýrslugerð sem einangrar skýrslugerð frá efnislegri innleiðingu gagnagjafa. Hann sýnir viðskiptahugtök fyrir tiltekin svið og virkni í skjámynd sem gerir frumhönnun og frekara viðhald á skýrslugerðarsniði skilvirkara.

#### <a name="format-components-for-outgoing-electronic-documents"></a><a name="FormatComponentOutbound"></a>Sniðsþáttur fyrir rafræn skjöl á útleið

Snið er skema skýrsluúttaks sem myndast á keyrslutíma. Skema samanstendur af eftirfarandi þáttum:

- Snið sem skilgreinir skipulag og innihald í rafrænu skjali á útleið sem er myndað á keyrslutíma.
- Gagnagjafar, sem ílagsfæribreytur notanda og gagnalíkön fyrir tiltekin svið sem nota valda líkanavörpun.
- Sniðsvörpun, sem safn bindingar fyrir gagnagjafa sniða sem eru með einstakar sniðseiningar sem tilgreina, á keyrslutíma, gagnaflæði og reglur um myndun úttakssniðs.
- Villuleitarsnið, sem hópur af samskipanlegum reglum sem stýra skýrslugerð á keyrslutíma, háð samhengi keyrslu. Til dæmis gæti verið regla sem stöðvar úttaksmyndun fyrir greiðslur lánardrottins og beitir undantekningu þegar tilteknar eigindir valins lánardrottins vantar, eins og númer bankareiknings.

Þáttur sniðs styður eftirfarandi aðgerðir:

- Stofnun skýrslugerðarúttaks sem einstakar skrár í mismunandi sniði, t.d. texti, XML, Microsoft Word-skjal eða vinnublað.
- Stofnun margra aðgreindra skráa og einnig að steypa þessum skrám saman í ZIP-skrár.

Sniðsþáttur gerir þér kleift að hengja við tilteknar skrár sem hægt er að nota í skýrslugerðarúttaki:

- Excel-vinnubækur Sem inniheldur vinnublað sem sem má nota sem sniðmát fyrir úttak á OPENXML vinnublaðssniði;
- Word-skrár sem innihalda skjal sem hægt er að nota sem sniðmát fyrir úttak í sniði Microsoft Word-skjals.
- Aðrar skrár sem geta verið felldar inn í úttakssnið sem fyrirfram skilgreindar skrár.

Eftirfarandi dæmi sýnir gagnaflæðið fyrir þessi snið.

[![Gagnaflæði fyrir sniðsþætti á útleið](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Til að keyra eina sniðsskilgreiningu fyrir rafræna skýrslugerð og búa til rafrænt skjal til að senda út verður þú að auðkenna vörpun skilgreiningarsniðsins.

#### <a name="format-components-for-incoming-electronic-documents"></a><a name="FormatComponentInbound"></a>Sniðsþættir fyrir rafræn skjöl á innleið

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
- Hægt er að endurraða þættinum úr XML-skrá og flytja inn í forritið sem nýja útgáfu ER-þáttar.

#### <a name="component-date-effectivity"></a>Dagsetning á virkni íhlutar

ER þáttarútgáfur eru virkar eftir dagsetningum. Hægt er að stilla dagsetninguna **Virkt frá** fyrir þátt rafrænnar skýrslugerðar þannig að hún tilgreini þá dagsetningu sem þátturinn verður virkur fyrir skýrsluferla. Lotudagsetning forrits er notuð til að skilgreina hvort þáttur er gildur fyrir framkvæmd. Nýjusta útgáfa er notuð fyrir skýrsluferli þegar fleiri en ein útgáfa er í gildi fyrir tiltekna dagsetningu.

#### <a name="component-access"></a>Aðgangur að þáttum

Aðgangur ER sniðþátta fer eftir ISO-lands-/ svæðiskóða stillingum. Þegar þessi stilling er auð fyrir valda útgáfu skilgreiningar sniðs, er hægt að nálgast sniðsþátt úr hvaða fyrirtæki sem er á keyrslutíma. Þegar þessi stilling inniheldur ISO lands-/ svæðiskóða, er sniðsþáttur tiltækur eingöngu frá fyrirtækjum þar sem aðalaðsetur er tilgreint fyrir einn sniðsþátt ISO lands-/svæðiskóða.

Mismunandi útgáfur af gagnasniðsþáttum mega vera með mismunandi stillingar ISO lands-/ svæðiskóða.

#### <a name="configuration"></a><a name="Configuration"></a>Stilling

Skilgreining rafrænnar skýrslugerðar er pökkun tiltekins þáttar í rafrænni skýrslugerð. Sá þáttur getur annaðhvort verið gagnalíkansþáttur eða sniðsþáttur. Stilling getur innihaldið mismunandi útgáfur þáttar rafrænnar skýrslugerðar. Hver stilling er merkt sem eign tiltekinnar stillingarveitu. Útgáfan **Drög** af stillingarþætti er má breyta þegar eigandi stillingar hefur verið valinn sem virkur veitandi í ER-stillingum forritsins.

Hver líkanaskilgreining inniheldur gagnalíkansþátt. Ný skilgreining sniðs getur komið frá tiltekinni skilgreiningu gagnalíkans. Í stillingatrénu birtist skilgreining sem er stofnuð sem undirliður upphaflegrar gagnalíkansstillingar.

Sniðsskilgreining sem er stofnuð inniheldur sniðsþátt. Gagnalíkansþáttur upphaflegrar stillingar líkans er sjálfkrafa settur inn í sniðsþátt undirliðsstillingar sem sjálfgefinn gagnagjafi.

Skilgreining ER er samnýtt fyrir forritsfyrirtækin.

#### <a name="provider"></a><a name="Provider"></a>Veita

ER-veitan er auðkenni aðila sem er notuð til að tilgreina höfund (eiganda) fyrir hverja ER-skilgreiningu. ER leyfir þér að að stjórna lista yfir veitendur skilgreininga. Skilgreiningarsnið sem eru gefin út fyrir rafræn skjöl sem hluti af Finance and Operations-lausninni eru merkt sem í eigu skilgreiningarveitu **Microsoft**.

Til að fræðast um hvernig á að skrá nýja þjónustuveitu rafrænnar skýrslugerðar skaltu spila verkleiðbeiningarnar **Stofna veitanda skilgreiningar í rafrænni skýrslugerð og merkja sem virkan** (hluti af viðskiptaferlinu **7.5.4.3 Komast yfir/þróa þætti fyrir upplýsingatækniþjónustu/lausnir (10677)**).

#### <a name="repository"></a><a name="Repository"></a>Geymsla

ER-gagnasafn vistar ER-skilgreiningar. Eftirfarandi ER-gagnasöfn eru studd sem stendur: 

- Samnýtt LCS-safn
- LCS-verk
- Skráakerfi
- RCS
- Operations-tilföng
- Altæk geymsla

Gagnasafnið **Samnýtt LCS-safn** veitir aðgang að lista yfir skilgreiningar innan samnýtts eignasafns í Lifecycle Services (LCS). Einungis er hægt að skrá þessa gerð af ER-gagnasafni fyrir Microsoft-þjónustuaðilann. Úr samnýtta LCS-eignasafninu er hægt að flytja nýjustu útgáfur af ER grunnstillingum inn í núgildandi tilvik.

Gagnageymsla **LCS-verks** veitir aðgang að lista yfir skilgreiningar ákveðins LCS-verks (eignasafn LCS-verks) sem var valið gagnageymsla var skráð. Rafræn skýrslugerð gerir þér kleift að hlaða upp samnýttum skilgreiningum úr núverandi tilviki í tiltekna geymslu fyrir **LCS-verk** . Einnig er hægt að flytja skilgreiningar úr gagnageymslu **LCS-verks** inn í núverandi tilvik af Finance and Operations-forritunum.

Gagnasafn **Skráakerfis** veitir aðgang að lista yfir skilgreiningar sem eru staðsettar sem xml-skrár í tiltekinni möppu í staðbundnu skráakerfi vélarinnar þar sem AOS-þjónustan er hýst. Nauðsynleg mappa er valin á skráningarstigi gagnasafns. Hægt er að flytja inn skilgreiningar úr gagnasafni **Skráakerfis** í núverandi tilviki. 

Athugið að þessi gagnasafnsgerð er aðgengileg í eftirfarandi umhverfi:

- Umhverfi í skýi sett upp í þróunarlegum tilgangi (inniheldur prufulíkön úr inniföldum pökkum)
- Umhverfi sett upp á staðnum (innanhúss)

Frekari upplýsingar er að finna í [Flytja inn skilgreiningar rafrænnar skýrslugerðar](./electronic-reporting-import-ger-configurations.md).

Gagnageymsla **RCS** veitir aðgang að lista yfir skilgreiningar á tilteknu tilviki [Skilgreiningarþjónustu (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) sem var valið á skráningarstigi gagnageymslu. Rafræn skýrslugerð gerir þér kleift að flytja inn skilgreiningar, sem er lokið eða eru samnýttar, úr völdu RCS-tilviki í núgildandi tilvik svo hægt sé að nota þær í rafrænni skýrslugerð.

Frekari upplýsingar er að finna í [Flytja inn skilgreiningar rafrænnar skýrslugerðar frá RCS](./rcs-download-configurations.md).

Gagnageymslan **Altæk geymsla** veitir aðgang að lista yfir skilgreiningar innan altækrar geymslu í [Skilgreiningarþjónustu](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration). Einungis er hægt að skrá þessa gerð af ER-gagnasafni fyrir Microsoft-þjónustuaðilann. Úr altækri geymslu er hægt að flytja nýjustu útgáfur af skilgreiningum rafrænnar skýrslugerðar inn í núverandi tilvik.

Frekari upplýsingar er að finna í [Flytja inn skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](./er-download-configurations-global-repo.md).

Gagnasafn fyrir **Rekstrartilföng** veitir aðgang að lista yfir skilgreiningar sem Microsoft, sem þjónustuaðili ER-skilgreininga, gefur út upphaflega sem hluta af forritslausninni. Þessar skilgreiningar er hægt að flytja inn í núverandi tilvik og nota fyrir rafræna skýrslugerð eða til að spila sýnishorn af verkefnaleiðbeiningum. Einnig er hægt að nota þær fyrir frekari staðfæringar og sérstillingar. Athugaðu að nýjustu útgáfur sem ER-skilgreiningar Microsoft veita er nauðsynlegt að flytja inn úr samnýttu LCS-eignasafni með því að nota samsvarandi ER-gagnasafn.

Hægt er að skrá nauðsynleg gagnasöfn **LCS-verks**, **Skráakerfis** og **Skilgreiningarþjónustu reglugerðar (RCS)**, hvert safn fyrir sig, fyrir hverja skilgreiningarveitu fyrir núgildandi tilvik. Hvert gagnasafn getur verið sérmerkt tiltekinni skilgreiningarveitu.

## <a name="supported-scenarios"></a>Studdar aðstæður

### <a name="building-a-data-model"></a>Byggja gagnalíkan

ER býður upp á hönnun líkana sem má nota til að byggja gagnalíkan fyrir tiltekin viðskiptasvið. Allir umdæmissértækir viðskiptaaðilar og tengsl milli þeirra er hægt að sýna í gagnalíkani sem stigskipt uppbygging. 

til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER hönnun gagnalíkan fyrir sértækt svið** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="translating-data-model-content"></a>Þýðing á innihaldi gagnalíkans

Hægt er að þýða innihald gagnalíkans (merki og lýsingar) yfir á önnur tungumál sem forritin styðja. Gott væri að þýða innihald gagnalíkans af eftirfarandi ástæðum:

- Til að gera það skiljanlegra á hönnunartíma fyrir sniðhönnuði sem tala önnur tungumál og nota gagnalíkanið fyrir gagnavörpun sniðsþátta.
- Til að gera innihaldið notendavænna á keyrslutíma, með því að birta tilkynningar og hjálp fyrir færibreytur á keyrslutíma og skilgreind villuleitarskilaboð (villur og viðvaranir) á því tungumáli sem innskráður notandi kýs.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Stilling gagna í líkanavörpunum fyrir skjöl á útleið

Er veitir hönnuð líkanavörpunar sem leyfir notendum að varpa gagnlíkönum sem þeir hafa hannað á tilteknar gagnaveitur forritsins. Gögnin verða flutt inn samkvæmt vörpuninni á keyrslutíma úr völdum gagnagjöfum í gagnalíkanið. Gagnalíkanið er svo notað sem útdráttargagnagjafi allra sniða í rafrænni skýrslugerð sem búa til rafræn skjöl á útleið. 

Spila **ER Skilgreining líkanavörpunar og velja gagnagjafa** og **ER vörpun gagnalíkans í valda gagnagjafa** verkleiðbeiningar (hluti af **7.5.4.3 Acquire/Develop IT þjónustu-/lausnaþættir (10677)** viðskiptaferli) til að kynna þér aðstæðurnar í smáatriðum.

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Stilling gagna í líkanavörpunum fyrir skjöl á innleið

Rafræn skýrslugerð hefur að geyma hönnun líkanavörpunar sem leyfir notendum að varpa gagnalíkönum sem þeir hafa hannað á tiltekna staði. Til dæmis er hægt að varpa gagnalíkönum í uppfæranlega gagnaþætti (töflur, gagnaeiningar og yfirlit). Gögnin verða uppfærð samkvæmt vörpuninni á keyrslutíma með því að nota gögnin úr gagnalíkaninu. Gagnalíkanið er útdráttargeymsla fyrir snið í rafrænni skýrslugerð og er því fullt af gögnum sem eru flutt inn úr rafrænum skjölum á innleið. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Geyma hannaðan þátt líkans sem líkanastillingu

ER getur geymt hannað gagnalíkan ásamt tengdum gagnavörpunum sem gagnaskilgreiningu gildandi tilviks. Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð skilgreiningar gagnalíkans (skilgreining líkans fyrir greiðslu)

Spila **ER Skilgreining líkanavörpunar til að velja gagnagjafa** verkleiðbeiningar (hluti af **7.5.4.3 Acquire/Develop IT þjónustu-/lausnaþættir (10677)** viðskiptaferli) til að kynna þér aðstæðurnar í smáatriðum.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Byggja snið sem notar gagnalíkan sem grunneiningu

Rafræn skýrslugerð styður sniðshönnun sem þú getur notað til að setja upp snið fyrir rafrænt skjal fyrir valið viðskiptasvæði með því að velja líkansþáttinn sem grunn. Sama sniðshönnun í rafrænni skýrslugerð býður upp á möguleika á að varpa stofnuðu sniði á valið gagnalíkanavörpunarsvæði sem gagnagjafa. 

Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER hönnun sniðs fyrir sértækt svið** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Byggja skilgreiningu til að mynda rafræn skjöl í OPENXML sniði vinnublaðs

Hægt er að nota sniðshönnun fyrir rafræna skýrslugerð til að búa til rafræn skjöl á vinnublaðssniðinu OPENXML. 

Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER stofna skilgreiningu fyrir skýrslur í OPENXML-sniði** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) . Notaðu Excel-skrána [Sniðmát fyrir greiðsluskýrslu (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx) sem sniðmát, sem hluta af verkefnaleiðbeiningunum við að flytja inn snið.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Að búa til stillingu til að mynda rafræn skjöl á Word-skjalssniðinu.

Hægt er að nota sniðshönnun fyrir rafræna skýrslugerð til að búa til rafræn skjöl á skjalssniði fyrir Word. Eftirfarandi skýringarmynd sýnir dæmi um þessa gerð sniðs. Athugaðu að þetta snið notar aftur fyrirliggjandi grunnstillingu fyrir rafræna skýrslugerð sem var upphaflega hönnuð til að búa til skýrsluúttakið á OPENXML-sniði.

Til að kynna þér aðstæðurnar í smáatriðum skaltu spila verkleiðbeiningarnar Rafræn skýrslugerð - Hannaðu stillingu til að búa til skýrslur á Microsoft WORD sniðinu (hluti af viðskiptaferlinu 7.5.4.3 Komast yfir/þróa þætti fyrir upplýsingatækniþjónustu/lausnir (10677)). Notaðu eftirfarandi Word-skrár sem sniðmát fyrir snið rafrænnar skýrslugerðar, sem hluta af verkleiðbeiningunum fyrir innflutning á sniðmáti.

- [Sniðmát greiðsluskýrslu (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Afmarkað sniðmát greiðsluskýrslu (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Að búa til stillingu til að flytja inn gögn úr rafrænum skjölum á innleið

Hægt er að nota sniðshönnun í rafrænni skýrslugerð til að lýsa rafrænu skjali sem er hugsað fyrir gagnainnflutning á annaðhvort XML eða textasniði. Hannaða sniðið er notað til að þátta skjal á innleið. Hægt er að nota vörpunarhönnun fyrir snið í rafrænni skýrslugerð til að skilgreina bindingu eininga hannaðs sniðs við gagnalíkanið. 

Til að kynna þér aðstæðurnar í smáatriðum skaltu spila verkleiðbeiningarnar Stofnaðu nauðsynlegar stillingar í rafrænni skýrslugerð til að flytja inn gögn úr utanaðkomandi skrá (hluti af viðskiptaferlinu 7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)). Notaðu eftirfarandi skrár til að spila þessar leiðbeiningar:

- [Stilling á gagnalíkani í rafrænni skýrslugerð (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [Sniðsskilgreining í rafrænni skýrslugerð (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Sýnishorn af skjali á innleið á XML-sniði (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Sýnishorn af vinnubók til að stýra gögnum skjala á innleið (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Geyma hannaðan sniðsþátt í skilgreiningarsniði

ER getur geymt hannað snið með skilgreindum gagnavörpunum sem sniðsskilgreiningu fyrir núverandi tilvik. Fyrrgreint sýnidæmi sýnir dæmi af þessari gerð skilgreiningarsniðs (**BACS (UK)**, sem er undireining á **greiðslulíkan** skilgreiningu). Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER hönnun sniðs fyrir sértækt svið** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Stilling Finance til að byrja að nota stofnað snið innanhúss

Hægt er að stilla forritið til að byrja að nota stofnað snið fyrir rafræna skýrslumyndun. Tilvísun í stofnaða stillingarsniðið ætti að skilgreina í stillingum tiltekins sviðs. Til dæmis til að byrja að nota sniðskilgreiningu Rafræn skýrslugerð fyrir rafrænar greiðslur lánadrottins á BACS sniði, ætti að vera vísað í skilgreiningarsniðið í tilteknum greiðslumátum.

Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Er nota snið til að mynda rafrænt skjal fyrir greiðslur** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

## <a name="handling-er-components"></a>Meðhöndlun ER þátta

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Birting ER þátta í LCS til að bjóða það út á við (staðfærsla)

Eigandi þáttar (líkan eða snið) sem hefur verið stofnað getur notað ER til að birta kláraða útgáfu þáttarins í LCS. Geymsla **LCS verks** fyrir gildandi ER stillingaveitu er krafist. Þegar staða fullunnar útgáfu þáttar er breytt úr **LOKIÐ** í **SAMNÝTT**, er útgáfan er birt í LCS. Þegar þáttur hefur verið birtur í LCS verður eigandi þess þáttar veitandi þjónustu til að styðja þennan þátt. T.d. ef þessi sniðsþáttur er hannaður til að búa til rafrænt skjal sem er krafist samkvæmt lögum (t.d. í samræmi við staðfærsluaðstæður), gerir þessi þjónusta ráð fyrir að halda sniðinu í samræmi við lögboðnar breytingar og hönnuðurinn muni gefa út nýjar útgáfur þegar styðja þarf nýjar lögbundnar kröfur. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Er hlaða upp skilgreiningu í Lifecycle Services** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Flytja þátt ER úr LCS til nota innan kerfis

ER gerir það mögulegt að flytja inn ER þætti úr LCS í núverandi tilvik. Geymslu af gerðinni **LCS verki** er krafist. Þegar rafrænn skýrsluþáttur hefur verið fluttur inn úr LCS í núverandi tilvik, verður eigandi tilviksins neytandi þjónustunnar sem eigandi (höfundur) innflutta þáttarins veitir. Til dæmis, ef sniðsþáttur er hannaður til að mynda úr tiltekið rafrænt skjal úr forritinu á sniði sem er sértækt fyrir land-/svæði (staðfærslu aðstæður), þá gerir notkun þessarar þjónustu ráð fyrir getu til að fá allar uppfærslur á sniðinu til að halda því í samræmi við lögboðnar kröfur. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Flytja inn skilgreiningu úr Lifecycle Services** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Byggja snið og velja annað snið sem grunn (sérsnið).

ER gerir þér kleift að stofna (leita út) nýjan þátt úr gildandi útgáfu af þætti (grunni) sem var flutt úr LCS. Til dæmis, notandi vill afleiða nýja snið sem á að innleiða sérstakar þarfir fyrir rafrænt skjal (til dæmis viðbótarreit eða yfirgripsmikla lýsing) til að styðja aðstæður sérsníðingar. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Uppfæra snið með innleiðingu nýs grunns fyrir það** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Uppfæra snið því að velja nýja útgáfu af grunnsniði (endurreikna grunn)

ER leyfir þér að taka sjálfkrafa í gagn breytingar á nýjustu útgáfu af þættinum grunngögn í gildandi drögum af afleiddum þætti. Þetta ferli kallast *endurreikningur*. Til dæmis, geta nýjar breytingar á reglum sem voru kynntar í síðastu útgáfu sniðsþáttar sem var flutt úr LCS verið sjálfkrafa sameinaðar við í sérsniðna útgáfu af þessu sniði rafrænna skjala. Allar breytingar sem ekki er hægt að sameina sjálfvirkt eru taldar árekstrar. Þessir árekstrar eru ætlaðir fyrir handvirka úrlausn í hönnunartæki fyrir viðkomandi þátt. Til að kynna þér aðstæðurnar í smáatriðum skaltu spila verkleiðbeiningarnar **ER Uppfæra snið með innleiðingu nýs grunns af því sniði** (hluti af **7.5.5.3 Komast yfir/þróa íhluti fyrir breytta upplýsingatækniþjónustu/lausnir (10683)** viðskiptaferli).

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Listi yfir skilgreiningar rafrænnar skýrslugerðar sem hafa verið gefnar út í Finance

Sífellt er verið að uppfæra Listann yfir skilgreiningar rafrænnar skýrslugerðar fyrir Finance. Opnið [Altæka geymsla](er-download-configurations-global-repo.md) til að fara yfir lista yfir skilgreiningar rafrænnar skýrslugerðar sem eru studdar. Í flýtiflipanum **Upplýsingar um niðurfellingu** er hægt að fara yfir upplýsingar um skilgreiningar sem hætt hefur verið við eða sem ekki er verið að viðhalda. 

![Efni altækrar geymslu síað á síðu skilgreiningageymslu](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Stofna skilgreiningar fyrir rafræna skýrslugerð](electronic-reporting-configuration.md)
- [Stjórnun á lífsferli grunnstillingar fyrir rafræna skýrslugerð](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
