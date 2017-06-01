---
title: "Yfirlit yfir Rafræna skýrslugerð"
description: "Í greininni má sjá yfirlit yfir verkfærið Rafræn skýrslugerð. Þar á meðal er að finna upplýsingar um lykilhugtök, sviðsmyndir sem Rafræn skýrslugerð styður og lista yfir snið sem hafa verið hönnuð og gefin út sem hluti af lausninni."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: caa9f4c73f4c6b5b7637b5b012bd9ed3b7dd6392
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-reporting-overview"></a>Yfirlit yfir Rafræna skýrslugerð

[!include[banner](../includes/banner.md)]


Í greininni má sjá yfirlit yfir verkfærið Rafræn skýrslugerð. Þar á meðal er að finna upplýsingar um lykilhugtök, sviðsmyndir sem Rafræn skýrslugerð styður og lista yfir snið sem hafa verið hönnuð og gefin út sem hluti af lausninni.

Rafræn skýrslugerð (ER) er verkfæri sem hægt er að nota til að skilgreina sniðið á rafrænum skjölum í samræmi við ákvæði laga mismunandi landa/svæða. ER (rafræn skýrslugerð) gerir þér kleift að stjórna þessum sniðum í lífsferli þeirra. Til dæmis er hægt taka í gagn nýja krafa samkvæmt reglum og getur myndað viðskiptaskjala í nauðsynlegu sniði til að skiptast rafrænt á upplýsingum við stjórnvöld, banka og aðrar aðilum. Vélar fyrir rafræna skýrslugerð eru ætlaðar fyrir viðskiptanotendur í stað þróara. Vegna þess að þú skilgreina snið, en ekki kóða, er ferli við að stofna og stilla snið fyrir rafræn skjöl fljótari og auðveldari. Á þessum tíma styður ER TEXT, XML og OPENXML snið vinnublaða. Hins vegar veitir viðbótar viðmót stuðning við fleiri snið.

## <a name="capabilities"></a>Geta
ER-vélin hefur eftirfarandi getu:

-   Það er eitt almennt verkfæri til rafrænnar skýrslugerðar á mismunandi lénum, og kemur í stað 20 mismunandi véla sem gera einhvers konar rafræna skýrslugerð fyrir Microsoft Dynamics 365 for Operations.
-   Það gerir snið á skýrslu einangrað úr núgildandi innleiðingu Microsoft Dynamics 365 for Operations. (Með öðrum orðum, snið gildir fyrir mismunandi útgáfur af Dynamics 365 for Operations.)
-   Hann styður stofnun sérsniðinnar sniða sem byggð er á upprunalegu sniði. Það felur í sér getu til að uppfæra sjálfkrafa sérsniðna snið þegar breytingar á upprunalegu snið eiga sér stað, vegna þess að kröfur um staðfærslu/sérsnið eru kynnt til leiks.
-   Verður það aðal viðtekna verkfærið til að styða við kröfur um staðfæringu í rafrænni skýrslugerð – bæði fyrir Microsoft sem og microsoft samstarfsaðila;
-   Það styður getu til að dreifa sniðum til viðskiptaaðila og viðskiptavini með Microsoft Dynamics Lifecycle Services (LCS).

## <a name="concepts"></a>Hugtök
### <a name="components"></a>Íhlutir

ER styður tvær gerðir íhluta **gagnalíkan** og **Snið**.

#### <a name="data-model-components"></a>Íhlutir gagnalíkana

Íhlutir gagnalíkans er óhlutbundin framsetning gagnaskipulagsins sem nota á til að lýsa ákveðnu viðskiptasviði í nægilegum smáatriðum til að uppfylla kröfur um skýrslugerð á því sviði. Íhlutir gagnalíkans samanstendur af eftirfarandi hluta:

-   Gagnalíkan sem hópur af svæðissértækum viðskiptaeiningum auk stigskiptra tengslaskilgreininga á milli þessara eininga;
-   Líkanavörpun sem tengir völdum Microsoft Dynamics 365 fyrir Operations gagnagjöfum við einstakar einingar gagnalíkans sem tilgreinir, við keyrslutíma, gagnaflæði og reglur viðskiptagagna við þætti gagnalíkans.

Viðskiptaeining gagnalíkans er birt sem geymir (skýrsla). Eiginleikar viðskiptaeininga eru sýndir sem gagnaatriði (svæði). Hvert gagnaatriði hefur einstakt heiti, merki, lýsingu og gildi. Hægt er að hanna virði hvers atriðis svo það sé viðurkennt sem strengur, heiltala, raunverulegt, dagsetning, tölusett, boole-gildi o.s.frv.  Þar að auki getur það verið önnur færsla eða færslulisti. Einstakur þáttur gagnalíkans getur innihaldið mörg stigveldi sviða sem eru tilgreind eftir viðskiptaeiningum auk líkanavörpunar sem styðja við sérstakt skýrslutengt gagnaflæði á keyrslutíma. Stigveldin verða aðgreind eftir einni færslu sem hefur verið valin sem rót líkanavörpunar. Til dæmis, Gagnalíkan fyrir greiðslusvið gæti stutt eftirfarandi varpanir:

-   Fyrirtæki -&gt; Lánardrottinn -&gt; Greiðslufærslur AP sviðs
-   Viðskiptavinur -&gt; Fyrirtæki -&gt; Greiðslufærslur AR sviðs

Athugið að viðskiptaeiningum (eins og Fyrirtæki og greiðslufærslur) eru hannaðar einu sinni. Mismunandi varpanir endurnota þær svo. Líkanavörpun hefur eftirfarandi getu:

-   Hægt er að nota mismunandi gagnagerðir Dynamics 365 for Operations sem gagnagjafa fyrir gagnalíkan. Til dæmis getur það notað töflur, gagnaeiningar, aðferðir eða upptalningar.
-   Það styður ílagsfæribreytur notanda sem má skilgreina sem gagnagjafa gagnalíkans þegar tilgreina þarf gögn á keyrslutíma.
-   Hann styður umbreytingu Dynamics 365 fyrir Operations gagna í áskilda hópa, síun, flokkun, og samlagningu gagna, og einnig að hengja við rökrétta útreiknaða reiti sem eru hannaðir í með formúlum sem eru eitthvað í líkingu við Microsoft Excel (fyrir nánari upplýsingar, sjá [formúluhönnuður í Rafræna skýrslugerð](general-electronic-reporting-formula-designer.md)).

[![Formúluritill á borð við Excel](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Eining gagnalíkans er hönnuð fyrir hvert viðskiptalén sem nota á sem sameinaðan gagnagjafa fyrir skýrslugerð sem einangrar skýrslugerð frá efnislegri innleiðingu Microsoft Dynamics 365 for Operations-gagnagjöfum, og stendur fyrir lén-sértæk viðskiptahugtök og aðgerðir á þann hátt sem gerir upphaflega hönnun skýrslugerðarsniðs og frekara viðhald skilvirkara.

#### <a name="format-components"></a>Sniðsþættir

Snið er skema skýrsluúttaks sem myndast á keyrslutíma. Skema samanstendur af eftirfarandi þáttum:

-   Snið sem skilgreinir skipulag og innihald í skjali rafrænnar skýrslugerðar sem er myndað á keyrslutíma.
-   Gagnagjafar sem ílagsfæribreytur notanda og lénsértæk gagnalíkön sem nota valda líkanavörpun;
-   Sniðsvörpun sem safn bindingar fyrir gagnagjafa sniða sem eru með einstakar sniðseiningar sem tilgreina á keyrslutíma gagnaflæði og reglur um myndun úttakssniðs;
-   Villuleit sniðs sem sett af skilgreinanlegum reglum sem stýra skýrslumyndun á keyrslutíma eftir samhengi keyrslu (til dæmis reglu sem stöðvar úttaksmyndun fyrir greiðslur til lánardrottins og beitir undantekningu þegar tilteknar eigindir valins lánardrottins vantar, eins og númer bankareiknings).

Þáttur sniðs styður eftirfarandi aðgerðir:

-   stofnun skýrslugerðarúttaks sem einstakar skrár í mismunandi sniði: texti, xml, vinnublað.
-   Stofnun margra skráa aðskilið, og einnig að steypa þessum skrám saman í ZIP-skrár.

Þáttur sniðs veitir getu til að hengja við tilteknar skrár sem má nota í skýrslugerðarúttaki:

-   Excel-vinnubækur Sem inniheldur vinnublað sem sem má nota sem sniðmát fyrir úttak á OPENXML vinnublaðssniði;
-   Aðrar skrár sem geta verið felldar inn í úttakssnið sem fyrirfram skilgreindar skrár.

#### <a name="component-versioning"></a>Sögugeymni íhlutar

Sögugeymnin er studd fyrir ER þætti. Eftirfarandi verkflæði er veitt fyrir stjórnun breytinga í ER þáttum:

-   Útgáfan sem var upphaflega stofnuð er merkt sem **DRÖG** útgáfu. Útgáfan er hægt að breyta og er tiltæk fyrir prófunarkeyrslu.
-   **DRÖG** útgáfa má umbreyta í **LOKIÐ** útgáfu. Hægt er að nota þessa útgáfu í staðbundna skýrslugerðarferli.
-   **LOKIÐ** útgáfa má umbreyta í **SAMNÝTT** útgáfu. Útgáfan er birt á LCS og hægt er að nota í altæku skýrslugerðarferli.
-   **SAMNÝTT** útgáfa MÁ umbreyta í **HÆTT VIÐ** útgáfu. Síðan er hægt að eyða þessari útgáfu.

Útgáfur sem eru annað hvort með** LOKIÐ** eða **SAMNÝTT** stöðu eru tiltækar fyrir önnur gagnaskipti. Þættir sem hefur þessar stöður getur haft þessar aðgerðir framkvæmd fyrir sig:

-   Þeim má raðað í xml-snið og flytja út úr Dynamics 365 fyrir Operations sem skrá í xml-sniði;
-   Þeim má endurraða úr xml-skrá og flytja inn í Dynamics 365 for Operations sem nýja útgáfu ER-þáttar.

#### <a name="component-date-effectivity"></a>Dagsetning á virkni íhlutar

ER þáttarútgáfur eru virkar eftir dagsetningum. **Virkt frá** dagsetning er hægt að skilgreina fyrir ER þátt til að tilgreina dagsetningu sem íhluturinn verður virkur á fyrir skýrsluferli. Dynamics 365 fyrir Operations lotudagsetning er notuð til að skilgreina hvort þáttur er gildur fyrir framkvæmd. Nýjusta útgáfa er notuð fyrir skýrsluferli þegar fleiri en ein útgáfa er í gildi fyrir tiltekna dagsetningu.

#### <a name="component-access"></a>Aðgangur að þáttum

Aðgangur ER sniðþátta fer eftir ISO-lands-/ svæðiskóða stillingum. Þegar þessi stilling er auð fyrir valda útgáfu skilgreiningar sniðs, er hægt að nálgast sniðsþátt úr hvaða Dynamics 365 fyrir Operations fyrirtæki sem er á keyrslutíma. Þegar þessi stilling inniheldur ISO lands-/ svæðiskóða, er sniðsþáttur tiltækur eingöngu frá Dynamics 365 fyrir Operations fyrirtækjum þar sem aðalaðsetur er tilgreint fyrir einn sniðsþátt ISO lands-/svæðiskóða. Mismunandi útgáfur af gagnasniðsþáttum mega vera með mismunandi stillingar ISO lands-/ svæðiskóða.

#### <a name="configuration"></a>Stilling

Stilling ER er pökkun af tilteknum þætti ER: annaðhvort **Gagnalíkan** eða **Snið**. Stilling kann að ininhalda mismunandi útgáfur af tilteknum ER-þætti. Hver stilling er merkt sem eign tiltekinnar stillingarveitu. **DRÖG** útgáfa af stillingarþætti er má breyta þegar eigandi stillingar hefur verið valinn sem virkur veitandi í Dynamics 365 for Operations ER-stillingum. Hver líkanaskilgreining Inniheldur  **gagnalíkan** þátt. Ný skilgreining sniðs getur komið frá  (verið afleidd) úr tiltekinni skilgreiningu gagnalíkans. skilgreining sniðs sem er stofnuð verða sýnd í skilgreiningartrénu sem undireining upphaflegrar skilgreiningar gagnalíkans. skilgreining sniðs sem er stofnuð inniheldur þátt **Sniðs**. Þáttur **Gagnalíkans** upphaflegrar skilgreiningar líkans verður sjálfkrafa sett inn í þátt **sniðs** fyrir skilgreiningu undirsniðs sem sjálfgefinn gagnagjafi. Skilgreining ER er samnýtt fyrir fyrirtæki í Dynamics 365 for Operations.

#### <a name="provider"></a>Veita

ER-veitan er auðkenni aðila sem er notuð til að tilgreina höfund (eiganda) fyrir hverja ER-skilgreiningu. ER leyfir þér að að stjórna lista yfir veitendur skilgreininga. Skilgreiningarsnið sem eru gefin út fyrir rafrænt skjal sem hluti af lausn Dynamics 365 for Operations eru merktar sem í eigu **Microsoft** skilgreiningarveitu.

#### <a name="repository"></a>Geymsla

ER-gagnasafn vistar ER-skilgreiningar. Eftirfarandi ER-gagnasöfn eru studd sem stendur: **Operations-tilföng** og **LCS-verk**. Tilfangageymsla Operations-tilfanga veitir aðgang að lista skilgreininga sem eru útgefnar sem hluti af Dynamics 365 for Operations lausnum frá Microsoft sem ER-skilgreiningarveita. Þessar stillingar er hægt að flytja inn í núverandi Dynamics 365 for Operations tilvik og nota fyrir rafræna skýrslugerð. Þær má einnig nota fyrir frekari staðfæringar og/eða sérstillingar. **LCS-verks** gagnasafn veitir aðgang að lista yfir skilgreiningar ákveðins LCS-verks (eignasafn LCS-verks) sem var valið á skráningarstigi gagnasafns. Rafræn skýrslugerð leyfir þér að hlaða upp samnýttar skilgreiningar úr núverandi Dynamics 365 for Operations tilviki í tilteknar **LCS-verks** gagnasöfn. Þú getur einnig flutt inn skilgreiningar úr úr tilteknu **LCS-verks** gagnasöfn í núverandi tilvik Dynamics 365 for Operations. Hægt er að skrá nauðsynlega **LCS verks** gagnasafn fyrir hverja skilgreiningarveitu fyrir gildandi tilvik Dynamics 365 for Operations sérstaklega. Hvert gagnasafn getur verið sérmerkt tiltekinni skilgreiningarveitu.

## <a name="supported-scenarios"></a>Studdar aðstæður
### <a name="building-a-data-model"></a>Byggja gagnalíkan

ER býður upp á hönnun líkana sem má nota til að byggja gagnalíkan fyrir tiltekin viðskiptasvið. Allir umdæmissértækir viðskiptaaðilar og tengsl milli þeirra er hægt að sýna í gagnalíkani sem stigskipt uppbygging.  Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð gagnalíkans (gagnalíkan á sviði greiðslu) [![Dæmi um gagnalíkan](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Til að kynna þér aðstæðurnar í smáatriðum skaltu spila verkefnaleiðbeiningar **ER hönnun gagnalíkan fyrir sértækt gagnalíkan** (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="translating-data-model-content"></a>Þýðing á innihaldi gagnalíkans

Hægt er að þýða innihald gagnalíkans (merki og lýsingar) yfir á önnur tungumál sem Dynamics 365 for Operations styður. Gott væri að þýða innihald gagnalíkans af eftirfarandi ástæðum:

-   á hönnunartíma, til að gera það skiljanlegra fyrir sniðhönnuði sem tala erlend tungumál sem nota gagnalíkan fyrir gagnavörpun sniðsþátta;
-   Á keyrslutíma, til að gera innihaldi notendavænna með því að birta tilkynningar og hjálp fyrir færibreytur á keyrslutíma, og einnig skilgreind staðfestingarskilaboð (villur, viðvaranir) á tungumáli þess sem er innskráður notandi Microsoft Dynamics 365 for Operations kýs.

Eftirfarandi skýringarmynd sýnir dæmi um hvernig innihald gagnalíkans má þýða úr ensku á japönsku. [![Innihald gagnalíkans á ensku](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![Innihald gagnalíkans þýtt á japönsku](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Stilling gagna í líkanavörpunum

Rafræn skýrslugerð veitir hönnuð líkanavörpunar sem leyfir notendum að varpa gagnlíkönum sem þeir hafa hannað á tilteknar gagnaveitur Dynamics 365 for Operations. Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð af vörpun gagnalíkans (**SEPA kreditfærsla** líkanavörpun fyrir gagnalíkan á sviði greiðslu) [![Dæmi um vörpun gagnalíkans ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Spila **Rafræn skýrslugerð, Skilgreining líkanavörpunar og velja gagnagjafa** og **ER vörpun gagnalíkans í valda gagnagjafa** verkleiðbeiningar (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) til að kynna þér aðstæðurnar í smáatriðum.

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Geyma hannaðan þátt líkans sem líkanastillingu

Rafræn skýrslugerð getur geymt hannað gagnalíkan ásamt tengdum gagnavörpunum sem gagnaskilgreiningu gildandi Microsoft Dynamics 365 for Operations tilviks. Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð skilgreiningar gagnalíkans (skilgreining líkans fyrir greiðslu) [![Dæmi um skilgreiningu gagnalíkans ](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Spila **Rafræn skýrslugerð Varpa gagnalíkani í valda gagnagjafa** verkleiðbeiningar (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) til að kynna þér aðstæðurnar í smáatriðum.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Byggja snið sem notar gagnalíkan sem grunneiningu

ER styður sniðshönnun sem þú getur notað til að setja upp snið fyrir ákveðið rafrænt skjal fyrir valið viðskiptasvæði því að velja líkanaþáttinn sem grunn. Sama ER sniðhönnun býður upp á möguleika á að varpa stofnuðu sniði á valið gagnalíkanavörpunarsvæði sem gagnagjafa. Eftirfarandi skýringarmynd sýnir dæmi um slíka gerð sniðs (skilgreiningarsniðið sem styður í **BACS** greiðslusnið fyrir Bretland). [![Dæmi um snið sem er með gagnalíkan sem grunn](./media/pic-format-1024x690.png)](./media/pic-format.png) Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Rafræn skýrslugerð Hanna lénasértæk snið** verkefnaleiðbeiningar (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Byggja skilgreiningu til að mynda rafræn skjöl í OPENXML sniði vinnublaðs

ER-Sniðshönnuður má nota til að byggja tiltekna rafræna skjalið á OPENXML sniði vinnublaðs. Eftirfarandi skýringarmynd sýnir dæmi um slíka gerð sniðs (skilgreining sniðs til að mynda OPENXML vinnublað með upplýsingum um valda greiðslubók):[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Rafræn skýrslugerð Stofna skilgreiningu fyrir skýrslur í OPENXML-sniði** verkefnaleiðbeiningar (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) . Nota neðangreinar Excel-skrár sem vísað er í sem snið til að hanna snið fyrir Rafræn skýrslugerð til að klára skrefið fyrir innflutning sniðmáts fyrir snið í þessum verkefnaleiðbeiningar: [Sniðmát greiðsluskýrslu (SampleVendPaymWsReport.xlsx](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Geyma hannaðan sniðsþátt í skilgreiningarsniði

Rafræn skýrslugerð getur geymt hannað snið með skilgreindum gagnavörpunum sem sniðsskilgreiningu fyrir núverandi tilvik Dynamics 365 for Operations. Fyrrgreint sýnidæmi sýnir dæmi af þessari gerð skilgreiningarsniðs (**BACS (UK)**, sem er undireining á **greiðslulíkan**skilgreiningu). Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER hönnun sniðs fyrir sértækt svið** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Stilling Dynamics 365 for Operations til að byrja að nota stofnuð snið innanhúss

Hægt er að stilla Dynamics 365 for Operations til að byrja að nota stofnað snið fyrir rafræna skýrslumyndun. Tilvísun í stofnaða stillingarsniðið ætti að skilgreina í stillingum tiltekins sviðs. Til dæmis til að byrja að nota sniðskilgreiningu Rafræn skýrslugerð fyrir rafrænar greiðslur lánadrottins á BACS sniði, ætti að vera vísað í skilgreiningarsniðið í tilteknum greiðslumátum, eins og sýnt er í eftirfarandi skýringamyndir: 

[![BACS (UK ) skilgreining á sniði](media/ger-bacs-uk-format-configuration.png) 

[![Vísað í BACS (UK) snið í greiðslumáta](media/ger-bacs-uk-format-method.png) 

Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Er nota snið til að mynda rafrænt skjal fyrir greiðslur** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

## <a name="handling-er-components"></a>Meðhöndlun ER þátta
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Birting ER þátta í LCS til að bjóða það út á við (staðfærsla)

Eigandi þáttar (líkan eða snið) sem hefur verið stofnað getur notað ER til að birta kláraða útgáfu þáttarins í LCS. Geymsla **LCS verks**fyrir gildandi ER stillingaveitu er krafist. Þegar staða fullunnar útgáfu þáttar er breytt úr **LOKIÐ** í **SAMNÝTT**, er útgáfan er birt í LCS. Þegar þáttur hefur verið birtur í LCS verður eigandi þess þáttar veitandi þjónustu til að styðja þennan þátt. T.d. ef þessi sniðsþáttur er hannaður til að búa til rafrænt skjal sem er krafist samkvæmt lögum (t.d. í samræmi við staðfærsluaðstæður), gerir þessi þjónusta ráð fyrir að halda sniðinu í samræmi við lögboðnar breytingar og hönnuðurinn muni gefa út nýjar útgáfur þegar styðja þarf nýjar lögbundnar kröfur. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Er hlaða upp skilgreiningu í Lifecycle Services** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Flytja þátt ER úr LCS til nota innan kerfis

Rafræn skýrslugerð gerir það mögulegt að flytja inn þætti Rafræn skýrslugerð úr LCS í núverandi tilvik Dynamics 365 for Operations. Geymslu af gerðinni **LCS verki** er krafist. Þegar þáttur Rafræn skýrslugerð hefur verið fluttur úr LCS í núverandi tilvik Dynamics 365 for Operations, verður eigandi þessa tilviks neytandi þjónustunnar sem er veitt af eiganda (höfundi) innflutts þáttar. Til dæmis, ef sniðsþáttur er hannaður til að mynda úr tiltekið rafrænt skjal úr Dynamics 365 for Operations á sniði sem er sértækt fyrir land-/svæði (staðfærslu aðstæður), þá gerir notkun þessarar þjónustu ráð fyrir getu til að fá allar uppfærslur á sniðinu til að halda því í samræmi við lögboðnar kröfur. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Flytja inn skilgreiningu úr Lifecycle Services** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Byggja snið og velja annað snið sem grunn (sérsnið).

ER gerir þér kleift að stofna (leita út) nýjan þátt úr gildandi útgáfu af þætti (grunni) sem var flutt úr LCS. Til dæmis, notandi vill afleiða nýja snið sem á að innleiða sérstakar þarfir fyrir rafrænt skjal (til dæmis viðbótarreit eða yfirgripsmikla lýsing) til að styðja aðstæður sérsníðingar. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Uppfæra snið með innleiðingu nýs grunns fyrir það** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Uppfæra snið því að velja nýja útgáfu af grunnsniði (endurreikna grunn)

ER leyfir þér að taka sjálfkrafa í gagn breytingar á nýjustu útgáfu af þættinum grunngögn í gildandi drögum af afleiddum þætti. Þetta ferli kallast *endurreikningur*. Til dæmis, geta nýjar breytingar á reglum sem voru kynntar í síðastu útgáfu sniðsþáttar sem var flutt úr LCS verið sjálfkrafa sameinaðar við í sérsniðna útgáfu af þessu sniði rafrænna skjala. Allar breytingar sem ekki er hægt að sameina sjálfvirkt, eru taldar árekstrar. Þessir árekstrar eru ætlaðir fyrir handvirka úrlausn í hönnunartæki fyrir viðkomandi þátt. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Uppfæra snið með innleiðingu nýs grunns fyrir það** leiðarvísi fyrir verk (hluti af **7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)** viðskiptaferli) .

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Listinn yfir skilgreiningar Rafræn skýrslugerð sem eru sendar í Dynamics 365 for Operations lausn
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
| Intrastat-líkan
                                    | Viðskiptaskýrslugjöf       |                                                   |                                                                    |
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



<a name="see-also"></a>Sjá einnig
--------

[Kröfur um staðfæringu - stofna Skilgreining fyrir rafræna skýrslugerð](electronic-reporting-configuration.md)

[Stjórnun á lífsferli fyrir stillingar Rafrænnar skýrslugerðar](general-electronic-reporting-manage-configuration-lifecycle.md)




