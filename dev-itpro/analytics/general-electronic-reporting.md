---
title: "Yfirlit yfir Rafræna skýrslugerð"
description: "Í greininni má sjá yfirlit yfir verkfærið Rafræn skýrslugerð. Þar á meðal er að finna upplýsingar um lykilhugtök, sviðsmyndir sem Rafræn skýrslugerð styður og lista yfir snið sem hafa verið hönnuð og gefin út sem hluti af lausninni."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: b3e8174d07c9b9fd4210486c369c640fe07c49eb
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-overview"></a>Yfirlit yfir Rafræna skýrslugerð

Í greininni má sjá yfirlit yfir verkfærið Rafræn skýrslugerð. Þar á meðal er að finna upplýsingar um lykilhugtök, sviðsmyndir sem Rafræn skýrslugerð styður og lista yfir snið sem hafa verið hönnuð og gefin út sem hluti af lausninni.

Rafræn skýrslugerð (ER) er verkfæri sem hægt er að nota til að skilgreina sniðið á rafrænum skjölum í samræmi við ákvæði laga mismunandi landa/svæða. ER (rafræn skýrslugerð) gerir þér kleift að stjórna þessum sniðum í lífsferli þeirra. Til dæmis er hægt taka í gagn nýja krafa samkvæmt reglum og getur myndað viðskiptaskjala í nauðsynlegu sniði til að skiptast rafrænt á upplýsingum við stjórnvöld, banka og aðrar aðilum. Vélar fyrir rafræna skýrslugerð eru ætlaðar fyrir viðskiptanotendur í stað þróara. Vegna þess að þú skilgreina snið, en ekki kóða, er ferli við að stofna og stilla snið fyrir rafræn skjöl fljótari og auðveldari. Á þessum tíma styður ER TEXT, XML og OPENXML snið vinnublaða. Hins vegar veitir viðbótar viðmót stuðning við fleiri snið.

## <a name="capabilities"></a>Geta
ER-vélin hefur eftirfarandi getu:

-   Hún stendur fyrir eina algengar verkfæri fyrir rafræna skýrslugerð í sitthvoru léni og skuldfært 20 mismunandi vélar sem vinna sumar rafræna skýrslugerð vegna Microsoft Dynamics 365 fyrir Aðgerðir.
-   Það gerir snið á skýrslu insulated úr núverandi Dynamics 365 fyrir Aðgerðir innleiðingu. (Með öðrum orðum, snið gildir fyrir mismunandi útgáfur af Dynamics 365 fyrir Aðgerðir.)
-   Hann styður stofnun sérsniðinnar sniða sem byggð er á upprunalegu sniði. Það felur í sér getu til að uppfæra sjálfkrafa sérsniðna snið þegar breytingar á upprunalegu snið eiga sér stað, vegna þess að kröfur um staðfærslu/sérsnið eru kynnt til leiks.
-   Verður það aðal viðtekna verkfærið til að styða við kröfur um staðfæringu í rafrænni skýrslugerð – bæði fyrir Microsoft sem og microsoft samstarfsaðila;
-   Það styður getu til að dreifa sniðum til viðskiptaaðila og viðskiptavini með Microsoft Dynamics Lifecycle Services (LCS).

## <a name="concepts"></a>Hugtök
### <a name="components"></a>Íhlutir

ER styður tvær gerðir íhluta **gagnalíkan ** og **Snið **.

#### <a name="data-model-components"></a>Íhlutir gagnalíkana

Íhlutir gagnalíkans er óhlutbundin framsetning gagnaskipulagsins sem nota á til að lýsa ákveðnu viðskiptasviði í nægilegum smáatriðum til að uppfylla kröfur um skýrslugerð á því sviði. Íhlutir gagnalíkans samanstendur af eftirfarandi hluta:

-   Gagnalíkan sem hópur af svæðissértækum viðskiptaeiningum auk stigskiptra tengslaskilgreininga á milli þessara eininga;
-   Gögn streyma vörpun tengla valinn Dynamics 365 fyrir gagnagjafa Aðgerðum í einstaka einingar gagnalíkan sem tilgreinir í keyrslutíma, líkan og reglur business data population fyrir virðislíkanið íhlut.

Viðskiptaeining gagnalíkans er birt sem geymir (skýrsla). Eiginleikar viðskiptaeininga eru sýndir sem gagnaatriði (svæði). Hvert gagnaatriði hefur einstakt heiti, merki, lýsingu og gildi. Hægt er að hanna virði hvers atriðis svo það sé viðurkennt sem strengur, heiltala, raunverulegt, dagsetning, tölusett, boole-gildi o.s.frv.  Þar að auki getur það verið önnur færsla eða færslulisti. Einstakur þáttur gagnalíkans getur innihaldið mörg stigveldi sviða sem eru tilgreind eftir viðskiptaeiningum auk líkanavörpunar sem styðja við sérstakt skýrslutengt gagnaflæði á keyrslutíma. Stigveldin verða aðgreind eftir einni færslu sem hefur verið valin sem rót líkanavörpunar. Til dæmis, Gagnalíkan fyrir greiðslusvið gæti stutt eftirfarandi varpanir:

-   Fyrirtækis -&gt; Lánardrottins -&gt; greiðslufærslur AP léns
-   Viðskiptavinur -&gt; Fyrirtækis -&gt; greiðslufærslur AR léns

Athugið að viðskiptaeiningum (eins og Fyrirtæki og greiðslufærslur) eru hannaðar einu sinni. Mismunandi varpanir endurnota þær svo. Líkanavörpun hefur eftirfarandi getu:

-   Hægt er að nota mismunandi Dynamics 365 fyrir gerðir Aðgerða sem gagnagjafa fyrir gagnalíkan. Til dæmis getur það notað töflur, gagnaeiningar, aðferðir eða upptalningar.
-   Það styður ílagsfæribreytur notanda sem má skilgreina sem gagnagjafa gagnalíkans þegar tilgreina þarf gögn á keyrslutíma.
-   Hann styður umbreytingarinnar Dynamics 365 fyrir Aðgerðir í þarf flokka, sía, raða og samlagningu gögn og líka að bæta við röklegt reiknuð svæði sem eru hannaðar með Microsoft Excel-þ.h formúlur (fyrir nánari upplýsingar, sjá [formúluhönnuður í Rafræna skýrslugerð](general-electronic-reporting-formula-designer.md)).

[![Excel-þ.h formúlu ritil](./media/pic-formula-1024x615.png)](./media/pic-formula.png) gögn líkans íhlutur er hannað fyrir hvert viðskiptaferli lén sem á að nota sem sameinuðum gagnagjafa fyrir skýrslugerð sem isolates skýrslugerð úr efnislegt innleiðingu Dynamics 365 fyrir gagnagjafa Aðgerðir og stendur fyrir tiltekin lén business hugtök og aðgerðir í skjámyndinni sem gerir skýrslugerð snið upphafleg hönnun og frekar viðhald skilvirkari.

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
-   ** DRÖG** útgáfa má umbreyta í **LOKIÐ** útgáfu. Hægt er að nota þessa útgáfu í staðbundna skýrslugerðarferli.
-   Í **LOKIÐ** útgáfu hægt að umbreyta í á **SAMNÝTTUM** útgáfu. Útgáfan er birt á LCS og hægt er að nota í altæku skýrslugerð ferli.
-   ** SAMNÝTT** útgáfa MÁ umbreyta í **HÆTT VIÐ** útgáfu. Síðan er hægt að eyða þessari útgáfu.

Útgáfur sem hafa annaðhvort ** LOKIÐ ** eða **SAMNÝTTUM** stöður eru tiltækar fyrir önnur gögn skipti á rafrænum. Þættir sem hefur þessar stöður getur haft þessar aðgerðir framkvæmd fyrir sig:

-   Þær má raðað í xml-snið og út úr Dynamics 365 fyrir Aðgerðir sem skrá í xml-sniði.
-   Þær má reserialized úr xml-skrá og flutt inn í Dynamics 365 fyrir Aðgerðir sem ný útgáfa ER íhlutar.

#### <a name="component-date-effectivity"></a>Dagsetning á virkni íhlutar

ER þáttarútgáfur eru virkar eftir dagsetningum. ** Virkt frá ** dagsetning er hægt að skilgreina fyrir ER þátt til að tilgreina dagsetningu sem íhluturinn verður virkur á fyrir skýrsluferli. Dynamics 365 setudagsetning aðgerða er notuð til að skilgreina íhlut er gild fyrir framkvæmd. Nýjusta útgáfa er notuð fyrir skýrsluferli þegar fleiri en ein útgáfa er í gildi fyrir tiltekna dagsetningu.

#### <a name="component-access"></a>Aðgangur að þáttum

Aðgangur ER sniðþátta fer eftir ISO-lands-/ svæðiskóða stillingum. Þegar þessi stilling er autt fyrir valda útgáfu snið skilgreiningar snið íhluta fæst frá hvaða Dynamics 365 Aðgerðir fyrirtækis í keyrslutíma. Þegar þessi stilling inniheldur ISO lands-/ svæðiskóða er íhlut snið er eingöngu tiltækur í Dynamics 365 fyrir fyrirtæki Aðgerðir sem hafa aðalaðsetur sem skilgreind er fyrir snið þáttar ISO lands/svæðiskóða. Mismunandi útgáfur af gagnasniðsþáttum mega vera með mismunandi stillingar ISO lands-/ svæðiskóða.

#### <a name="configuration"></a>Stilling

Stilling ER er pökkun af tilteknum þætti ER: annaðhvort **Gagnalíkan ** eða **Snið**. Stilling kann að ininhalda mismunandi útgáfur af tilteknum ER-þætti. Hver stilling er merkt sem eign tiltekinnar stillingarveitu. Í **DRÖG** útgáfu er hluti af skilgreiningu er hægt að breyta þegar eigandi skilgreiningar hefur verið valin sem sem virka veitunnar í stillingum í Dynamics 365 aðgerða ER. Hver líkanaskilgreining Inniheldur  **gagnalíkan** þátt. Ný skilgreining sniðs getur komið frá  (verið afleidd) úr tiltekinni skilgreiningu gagnalíkans. skilgreining sniðs sem er stofnuð verða sýnd í skilgreiningartrénu sem undireining upphaflegrar skilgreiningar gagnalíkans. skilgreining sniðs sem er stofnuð inniheldur þátt **Sniðs **. Þáttur **Gagnalíkans ** upphaflegrar skilgreiningar líkans verður sjálfkrafa sett inn í þátt **sniðs** fyrir skilgreiningu undirsniðs sem sjálfgefinn gagnagjafi. ER skilgreining er samnýtt fyrir Dynamics 365 fyrir fyrirtæki Aðgerðir.

#### <a name="provider"></a>Veita

ER-veitan er auðkenni aðila sem er notuð til að tilgreina höfund (eiganda) fyrir hverja ER-skilgreiningu. ER leyfir þér að að stjórna lista yfir veitendur skilgreininga. Snið skilgreininga sem eru gefnar út til rafræn skjöl sem hluti af Dynamics 365 fyrir lausn Aðgerðir eru merktar sem eigu í **Microsoft** veitandi skilgreiningar.

#### <a name="repository"></a>Geymsla

ER-gagnasafn vistar ER-skilgreiningar. Eftirfarandi gerðir ER repositories eru studdir sem stendur: **rekstrartilföngum** og **LCS verks**. Í ** Aðgerðir tilföng ** geymslu veitir aðgang að lista yfir skilgreininga sem eru losaðar sem hluti af Dynamics 365 fyrir lausn Aðgerðir Microsoft sem veitandi skilgreiningar sem ER. Þessar skilgreiningar getur verið flutt inn í gildandi Dynamics 365 fyrir tilvik Aðgerðir og notað fyrir rafræna skýrslugerð. Þær má einnig nota fyrir frekari staðfæringar og/eða sérstillingar. **LCS-verks** gagnasafn veitir aðgang að lista yfir skilgreiningar ákveðins LCS-verks (eignasafn LCS-verks) sem var valið á skráningarstigi gagnasafns. ER gerir kleift að senda inn samnýtta skilgreiningar úr núverandi Dynamics 365 fyrir tilvik Aðgerða á ákveðnum **LCS verks** geymslunni. Einnig er hægt að flytja inn afbrigði úr ákveðnum **LCS verks** geymslu í gildandi Dynamics 365 fyrir tilvik Aðgerðir. Nauðsynleg **LCS verks** repositories er hægt að skrá sérstaklega fyrir hvern veitandi skilgreiningar á gildandi Dynamics 365 fyrir tilvik Aðgerðir. Hvert gagnasafn getur verið sérmerkt tiltekinni skilgreiningarveitu.

## <a name="supported-scenarios"></a>Studdar aðstæður
### <a name="building-a-data-model"></a>Byggja gagnalíkan

ER býður upp á hönnun líkana sem má nota til að byggja gagnalíkan fyrir tiltekin viðskiptasvið. Allir umdæmissértækir viðskiptaaðilar og tengsl milli þeirra er hægt að sýna í gagnalíkani sem stigskipt uppbygging.  Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð gagnalíkans (gagnalíkan á sviði greiðslu) [![Dæmi um gagnalíkan](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) kynnast upplýsingar í þessu dæmi, að spila á **Hönnun ER tiltekinn gagnalíkan lén** leiðarvísi fyrir verk (hluti á **7.5.4.3 Acquire/Hönnunar HANA/serviceslausn íhluti (10677)** viðskiptaferli).

### <a name="translating-data-model-content"></a>Þýðing á innihaldi gagnalíkans

Innihald framleiðslulíkans gögn (merki og lýsingar) hægt að þýða öðrum tungumálum sem styður Dynamics 365 aðgerða. Gott væri að þýða innihald gagnalíkans af eftirfarandi ástæðum:

-   á hönnunartíma, til að gera það skiljanlegra fyrir sniðhönnuði sem tala erlend tungumál sem nota gagnalíkan fyrir gagnavörpun sniðsþátta;
-   Á keyrslutíma, til að gera innihaldi fleiri notanda stutt af ráðlegginguna kvaðningar og hjálp fyrir færibreytur keyrslu tíma, og einnig skilgreint villuleit skilaboð (villur og viðvaranir) á tungumálinu sem í augnablikinu skráður inn á Dynamics 365 fyrir Aðgerðir sem notandinn vill

Eftirfarandi skýringarmynd sýnir dæmi um hvernig innihald gagnalíkans má þýða úr ensku á japönsku. [![Gögn líkans efni á Ensku](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png)[![Gögn Japanese þýða innihald líkans](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Stilling gagna í líkanavörpunum

ER býður upp á hönnuður líkanavörpunar svo að notendur varpa líkön gögn sem þeir hafa verið hannaðar tiltekna Dynamics 365 fyrir gagnagjafa Aðgerðir. Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð af vörpun gagnalíkans (**SEPA kreditfærsla** líkanavörpun fyrir gagnalíkan á sviði greiðslu) [![Dæmi um gagnalíkanavörpun ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png)Að kynnast smáatriði í þessu dæmi, spila á **SKAL Tilgreina líkanavörpun og velja gagnagjafa** og **gagnalíkan Vörpun ER í valda gagnagjafa** verk leiðbeiningar (hluti í **7.5.4.3 Acquire/Hönnunar HANA/serviceslausn íhluti (10677)** viðskiptaferli).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Geyma hannaðan þátt líkans sem líkanastillingu

ER hægt að geyma hannað gagnalíkan með tengdum gögnum varpanir sem skilgreiningu sem líkanið á gildandi Dynamics 365 fyrir tilvik Aðgerðir. Eftirfarandi skýringarmynd sýnir Dæmi sem samanstendur af þessari gerð skilgreiningar gagnalíkans (skilgreining líkans fyrir greiðslu) [![Dæmi um líkan afbrigði gögn ](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png)kynnast upplýsingar í þessu dæmi, að spila á **gagnalíkan Vörpun ER í valda gagnagjafa** leiðarvísi fyrir verk (hluti í **7.5.4.3 Acquire/Hönnunar HANA/serviceslausn íhluta (10677)** viðskiptaferli).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Byggja snið sem notar gagnalíkan sem grunneiningu

ER styður sniðshönnun sem þú getur notað til að setja upp snið fyrir ákveðið rafrænt skjal fyrir valið viðskiptasvæði því að velja líkanaþáttinn sem grunn. Sama ER sniðhönnun býður upp á möguleika á að varpa stofnuðu sniði á valið gagnalíkanavörpunarsvæði sem gagnagjafa. Eftirfarandi skýringarmynd sýnir dæmi um slíka gerð sniðs (skilgreiningarsniðið sem styður í **BACS** greiðslusnið fyrir Bretland). [![Dæmi um snið sem hefur gagnalíkanið sem grunneiningu](./media/pic-format-1024x690.png)](./media/pic-format.png) kynnast upplýsingar í þessu dæmi, að spila á **sniði umdæmi SKAL Hönnun** leiðarvísi fyrir verk (hluti í **7.5.4.3 Acquire/Hönnunar HANA/serviceslausn íhluta (10677)** viðskiptaferli).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Byggja skilgreiningu til að mynda rafræn skjöl í OPENXML sniði vinnublaðs

ER-Sniðshönnuður má nota til að byggja tiltekna rafræna skjalið á OPENXML sniði vinnublaðs. Eftirfarandi skýringarmynd sýnir dæmi um slíka sniði (afbrigði snið til að búa til vinnublað OPENXML með upplýsingum um valda greiðslubók):[![Pic-ER-snið-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) kynnast upplýsingar í þessu dæmi, að spila á **SKAL Stofna afbrigði fyrir skýrslur OPENXML sniði** leiðarvísi fyrir verk (hluti í **7.5.4.3 Acquire/Hönnunar HANA/serviceslausn íhluti (10677)** viðskiptaferli). Nota sem vísað er til fyrir neðan excel-skráin sem sniðmát sniðs vefsíðunni ER til að ljúka skrefinu snið sniðmáts fyrir innflutning á þessa leiðarvísi fyrir verk: [Sniðmát fyrir Skýrslu Greiðslunnar (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Geyma hannaðan sniðsþátt í skilgreiningarsniði

ER hægt að geyma designed snið og vörpununum skilgreindrar gögn sem sníða skilgreiningu á gildandi Dynamics 365 fyrir tilvik Aðgerðir. Fyrrgreint sýnidæmi sýnir dæmi af þessari gerð skilgreiningarsniðs (**BACS (UK)**, sem er undireining á **greiðslulíkan **skilgreiningu). Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER hönnun sniðs fyrir sértækt svið ** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Skilgreining Dynamics 365 aðgerða til að byrja að nota innan kerfis stofna snið

Hægt er að skilgreina dynamics 365 aðgerða til að byrja að nota stofna snið fyrir rafrænar skýrslur. Tilvísun í stofnaða stillingarsniðið ætti að skilgreina í stillingum tiltekins sviðs. Til dæmis til að byrja að nota skilgreiningu ER snið fyrir rafrænar greiðslur lánadrottins BACS sniði, skilgreiningarsniðið ætti að vera vísað í tiltekinn greiðslumáta, eins og sýnt er í eftirfarandi skýringamyndir: 

[![Sníða skilgreiningu BACS (UK)](media/ger-bacs-uk-format-configuration.png) 

[![Vísa í snið fyrir BACS (UK) í greiðslumáta](media/ger-bacs-uk-format-method.png) 

Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Er nota snið til að mynda rafrænt skjal fyrir greiðslur** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

## <a name="handling-er-components"></a>Meðhöndlun ER þátta
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Birting ER þátta í LCS til að bjóða það út á við (staðfærsla)

Eigandi þáttar (líkan eða snið) sem hefur verið stofnað getur notað ER til að birta kláraða útgáfu þáttarins í LCS. Geymsla **LCS verks **fyrir gildandi ER stillingaveitu er krafist. Þegar staða fullunnar útgáfu þáttar er breytt úr **LOKIÐ** í **SAMNÝTT**, er útgáfan er birt í LCS. Þegar þáttur hefur verið birtur í LCS verður eigandi þess þáttar veitandi þjónustu til að styðja þennan þátt. T.d. ef þessi sniðsþáttur er hannaður til að búa til rafrænt skjal sem er krafist samkvæmt lögum (t.d. í samræmi við staðfærsluaðstæður), gerir þessi þjónusta ráð fyrir að halda sniðinu í samræmi við lögboðnar breytingar og hönnuðurinn muni gefa út nýjar útgáfur þegar styðja þarf nýjar lögbundnar kröfur. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **Er hlaða upp skilgreiningu í Lifecycle Services** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Flytja þátt ER úr LCS til nota innan kerfis

ER gerir það mögulegt að flytja ER íhluti úr LCS núverandi Dynamics 365 fyrir tilvik Aðgerðir. Geymslu af gerðinni **LCS verki** er krafist. Þegar ER íhluta hefur verið flutt inn úr LCS í gildandi Dynamics 365 fyrir tilvik Aðgerðir, verður eiganda tilvik consumer þjónustu leggi eiganda (höfund) innfluttu íhluta. Til dæmis, ef íhlut snið er hannað til að mynda rafræna sérstakt skjal Dynamics 365 aðgerða sniði lands/svæðis-bundnar (staðfærslu aðstæður), gert er ráð fyrir að consumer þjónustu er hægt að fá allar uppfærslur sem eru gerðar á sniði, til að halda kennum legislative þörfum. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Flytja inn skilgreiningu úr Lifecycle Services** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Byggja snið og velja annað snið sem grunn (sérsnið).

ER gerir þér kleift að stofna (leita út) nýjan þátt úr gildandi útgáfu af þætti (grunni) sem var flutt úr LCS. Til dæmis, notandi vill afleiða nýja snið sem á að innleiða sérstakar þarfir fyrir rafrænt skjal (til dæmis viðbótarreit eða yfirgripsmikla lýsing) til að styðja aðstæður sérsníðingar. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Uppfæra snið með innleiðingu nýs grunns fyrir það ** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Uppfæra snið því að velja nýja útgáfu af grunnsniði (endurreikna grunn)

ER leyfir þér að taka sjálfkrafa í gagn breytingar á nýjustu útgáfu af þættinum grunngögn í gildandi drögum af afleiddum þætti. Þetta ferli kallast *endurreikningur*. Til dæmis, geta nýjar breytingar á reglum sem voru kynntar í síðastu útgáfu sniðsþáttar sem var flutt úr LCS verið sjálfkrafa sameinaðar við í sérsniðna útgáfu af þessu sniði rafrænna skjala. Allar breytingar sem ekki er hægt að sameina sjálfvirkt, eru taldar árekstrar. Þessir árekstrar eru ætlaðir fyrir handvirka úrlausn í hönnunartæki fyrir viðkomandi þátt. Til að kynna þér aðstæðurnar í smáatriðum skaltu Spila **ER Uppfæra snið með innleiðingu nýs grunns fyrir það ** leiðarvísi fyrir verk (hluti af **7.5.4.3 Acquire/Develop IT service/solution components (10677)** viðskiptaferli) .

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Listinn ER skilgreininga sem eru sendar í Dynamics 365 fyrir Aðgerðir lausn
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


