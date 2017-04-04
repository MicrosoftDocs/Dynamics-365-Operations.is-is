---
title: "Viðtökustaður rafrænnar skýrslugerðar"
description: "Hægt er að skilgreina áfangastað inn fyrir hverja skilgreiningarsnið Rafrænnar skýrslugerðar (ER) og íhlut úttaks þess (möppu eða í skrá). Notendur sem fá viðeigandi aðgangsheimildir geta einnig breytt stillingar fyrir áfangastað á keyrslutíma. Þessi skrá útskýrir áfangastaðastjórnun rafrænnar skýrslugerðar, gerðir áfangastaða sem eru studdar, og öryggisatriði."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Viðtökustaður rafrænnar skýrslugerðar

Hægt er að skilgreina áfangastað inn fyrir hverja skilgreiningarsnið Rafrænnar skýrslugerðar (ER) og íhlut úttaks þess (möppu eða í skrá). Notendur sem fá viðeigandi aðgangsheimildir geta einnig breytt stillingar fyrir áfangastað á keyrslutíma. Þessi skrá útskýrir áfangastaðastjórnun rafrænnar skýrslugerðar, gerðir áfangastaða sem eru studdar, og öryggisatriði.

Rafræn skýrslugerð (ER) skilgreiningar sniðs innihalda yfirleitt minnst einn frálagsíhlut: skrá. Skilgreiningar innihalda yfirleitt margar frálagsíhluti skráa af mismunandi gerðum (t.d. XML, TXT eða XLSX) sem eru flokkaðar í annað hvort í einni möppu eða margar möppur. Stjórnun áfangastaðar Rafrænnar skýrslugerðar gerir kleift að forstilla hvað gerist þegar hver íhlutur er keyrður. Að sjálfgefnu þegar afbrigði er keyrð, birtist svargluggi sem gerir kleift að notandinn er að vista eða opna skrána. Sama hegðun er einnig notuð þegar þú flytur inn skilgreiningu rafrænnar skýrslugerðar og skilgreinir ekki tilteknu áfangastaði fyrir hana. Eftir á ákvörðunarstað hefur verið stofnuð fyrir aðal frálagsíhlut, hnekkir sá ákvörðunarstað sjálfgefinni hegðun og möppu eða skráin er send samkvæmt stillingum áfangastaðar.

## <a name="availability-and-general-prerequisites"></a>Framboð og almenn skilyrði
Áfangastaði virkni ER ekki tiltækt í Microsoft Dynamics 365 til losunar 7,0 Aðgerðir (Febrúar 2016). Þess vegna verður að setja upp Microsoft Dynamics 365 aðgerða (Nóvember 2016 losun) sem nota á allar aðgerðir sem lýst er í þessu efnisatriði. Einnig er hægt að setja upp einn af eftirfarandi skilyrðum. Hins vegar huga þessar aukaaðsetur veita áfangastað reynslu fleiri takmörkuð ER.

-   Microsoft Dynamics 365 fyrir Aðgerðir útgáfa forrits 7.0.1 (Maí 2016)
-   Stjórnun áfangastaður fyrir rafræna skýrslugerð [bráðabót forrits](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Hægt er að setja upp áfangastaði aðeins fyrir skilgreiningar rafrænnar skýrslugerðar sem hafa verið fluttar inn, og fyrir sniðin sem eru tiltækir í **skilgreiningar rafrænnar skýrslugerðar** síðu.

## <a name="overview"></a>Yfirliti
ER áfangastað stjórnun aðgerðir eru tiltækar á **fyrirtækisstjórnun**&gt;**Rafræna skýrslugerð**. Hér er hægt að hnekkja sjálfgefna hegðun fyrir skilgreiningu. Innfluttar skilgreiningar eru ekki sýnd hér fyrr en smellt er á **Nýtt** og síðan, í á **Tilvísun** reit, skal velja skilgreiningu til að stofna stillingar fyrir áfangastað fyrir.

[![Velja skilgreiningu í svæðinu Tilvísun](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Eftir tilvísun hefur verið stofnað, er hægt að stofna skrá áfangastaðar fyrir hverja möppu eða í skrá. 

[![Stofna skrá áfangastaðar](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Athugið **: hægt er að stofna eina áfangastað fyrir hverja frálagsskrá af sama sniði, eins og möppu eða skrá sem er valin í **skrárnafn ** reit. Hægt er að virkja og óvirkja einstaka áfangastaði fyrir skrá áfangastaðar í sem **stillingar fyrir Áfangastað** svarglugga. **Stillingar** hnappinn er notuð til að stjórna áfangastaði fyrir valinn áfangastað skrár. Í **stillingar fyrir Áfangastað** svarglugganum er hægt að stjórna hvern ákvörðunarstað sérstaklega með því að stilla **Virkt** valkost fyrir hana.

[![Áfangastaður svarglugga stillingar](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Gerðir áfangastaða
Ýmsar gerðir áfangastaði eru studd. Þú getur virkjað eða óvirkjað allar gerðir á sama tíma. Á þennan hátt er annað hvort hægt að gera ekkert eða senda íhlutinn á allar skilgreinda áfangastaði. Eftirfarandi kaflar lýsa áfangastaði sem eru studdar.

### <a name="email-destination"></a>Áfangastður tölvupósts

Setja **Virkt ** til **Já** til að senda frálagsskrá með tölvupósti. Þegar þessi valkostur er gerður virkur er hægt að tilgreina viðtakendur tölvupósts og breyta efni og meginmáli tölvupóstskeytis. Hægt er að setja upp fasta texta fyrir tölvupóst efni og meginmál, eða hægt er að nota formúlur ER til að stofna vöruþekjuna texta tölvupósts. Hægt er að skilgreina netföng fyrir ER skilgreint á tvo vegu. Hægt er að ljúka við skilgreiningu á sama hátt sem lýkur Prenta stjórnun eiginleikinn Dynamics 365 fyrir Aðgerðir í því. Einnig er hægt að leysa tölvupóstfang með því að nota beina tilvísun afbrigðið ER gegnum formúlu.

### <a name="email-address-types"></a>Gerðir tölvupóstur aðseturs

Þegar smellt er á **Breyta** til á **Til** eða **Cc** er í **í Tölvupósti til** birtist svarglugginn. Hægt er að velja þá gerð netfang til að nota.

[![Í svarglugganum í tölvupósti](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Prentstýring

Ef valið er **Prentstýringu tölvupósti** gerð er hægt að færa inn fast netföng í í **Til** svæði. Til að nota netföng sem ekki eru kostnaðarjafnaðar, verður að velja upprunagerð tölvupósti skrá áfangastaðar. Eftirfarandi gildi eru studd: **Viðskiptavinar**, **Lánardrottins**, **Viðfang**, **Tengilið**, **Keppinauta**, **Starfsmanns**, **Umsækjanda**, **Væntanlegs lánardrottins**, og **lánardrottins Án**. Eftir upprunagerð í tölvupósti er hnappurinn áfram að á **Tölvupósti upprunalykil** svæði til að opna í ** formúluhönnuður ** skjámynd. Hægt er að nota þessa skjámynd til að tengja formúlu sem táknar valda aðilalykil áfangastað tölvupóst.

[![Skilgreina gerð tölvupósti prentstýringar](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Athugið að formúlur eru við tilgreindar fyrir skilgreiningu rafrænnar skýrslugerðar. Í **formúla**, Færið inn skjalbundna tilvísun í viðskiptavin eða lánardrottinn gerð aðila. Í stað þess að slá inn, hægt að finna gagnaveituhnút sem stendur fyrir lykil viðskiptavinar eða lánardrottins, og smella á **bæta Við gagnaveitu ** hnappinn til að uppfæra formúlu. Dæmi: Ef ISO 20022 skilgreining millifærslu fjármuna er notuð, hnúta sem standa fyrir lykil lánardrottins er  **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Annars að færa inn strenggildi, eins og **DE-001**, til að vista formúlu.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Í á **í Tölvupósti til** svarglugganum, smellið á karfa endurvinna hliðina á í **Tölvupósti upprunalykil** svæði til að eyða lausninni formúlu fyrir upprunalykil tölvupóstur. Einnig er hægt að opna formúluhönnuður til að breyta formúlu sem áður voru vistaðar. Úthluta netföngum, að smella á **Breyta** til að opna í **netföng Úthluta** svarglugga.

[![Úthluta netföng fyrir tölvupóst áfangastaðar](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Skilgreiningartölvupóstur

Notið þessa gerð netfang ef skilgreiningin sem nota hnút í gagnagjafa sem táknar tölvupóstfang. Hægt er að nota gagnagjafa og aðgerðir í hönnuði formúlu til að fá rétt sniðnar tölvupóstfang.

[![Úthluta inn gagnagjafa tölvupósti aðsetur fyrir tölvupóst áfangastaðar](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Athugasemd:** SMTP-samskiptareglur (SMTP) þjóns verða að vera skilgreindar og tiltækar. Hægt er að tilgreina SMTP þjóns í Dynamics 365 fyrir Aðgerðir á **kerfisstjórnun**&gt;**Uppsetningu**&gt;**Tölvupósti**&gt;**Tölvupósti færibreytur**.

### <a name="archive-destination"></a>áfangastaður skjalasafns

Hægt er að nota þennan valkost til að senda frálag annað hvort á Microsoft SharePoint-möppu eða Microsoft Azure Geymslu. Stilla **Virkt** á **Já ** til að senda frálag á áfangastað sem er skilgreind með völdu skjalagerðina. einungis gerð skjals þar sem flokksins er stillt á **Skrá** eru tiltækar til vals. Skilgreina gerðir skjala í **fyrirtækisstjórnun**&gt;**Skjalastjórnun**&gt;**Skjalagerðir**. Skilgreining fyrir áfangastaði rafrænnar skýrslugerðar er sú sama og skilgreiningin fyrir skjalastjórnunarkerfið.

[![Síða gerðir skjala](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Staðsetning ákvarðar hvar skráin er vistuð. Eftir það **Safn** áfangastaður er virkjaður er hægt er að vista niðurstöður framkvæmdar afbrigði í safninu Vinnslu. Hægt er að skoða niðurstöður á **fyrirtækisstjórnun**&gt;**Rafræna skýrslugerð**&gt;**Rafræna skýrslugerð skjalaðar vinnslur**. **Athugasemd:** hægt er að velja skjalagerðina fyrir safn Vinnslu í Dynamics 365 fyrir Aðgerðir í **fyrirtækisstjórnun**&gt;**Vinnusvæða**&gt;**Rafræna skýrslugerð**&gt;**Rafræna skýrslugerð færibreytur**.

#### <a name="sharepoint"></a>SharePoint

Hægt er að vista skrá í möppu merktu SharePoint. Tilgreina sjálfgefinn þjón SharePoint á **fyrirtækisstjórnun**&gt;**Skjalastjórnun**&gt;**Færibreytur skjalastjórnunar**á í **SharePoint** flipa. Eftir að SharePoint-möppu er skilgreint hægt að velja það sem möppuna þar sem úttakið ER að vista fyrir gerð skjals. 

[![Velja SharePoint-möppu](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure-geymsla

Þegar staðsetning gerðar skjals er stillt á **skjalasafn**, er hægt að vista skrá í Azure Geymslu.

### <a name="file-destination"></a>Viðtökustaður skráar

Ef sett **Virkt** til **Já**, sem opna eða vista svargluggi birtist þegar afbrigði er lokið.

### <a name="screen-destination"></a>Áfangastaður skjánum

Ef sett **Virkt** til **Já**, forskoðun úttak er stofnuð. Hægt er að skoða sumar skrárgerðir XML, TXT eða PDF, beint í vafra glugga. Fyrir önnur skrá slíkar Microsoft Excel eða Word, Microsoft Office netþjónustuna notaður.

### <a name="power-bi-destination"></a>Áfangastaður power BI

Setja **Virkt** til **Já** nota samskipan ER til að útbúa flutning gagna úr tilvikum Dynamics 365 aðgerða Microsoft Power BI þjónustu. Flutt skrárnar eru vistaðar í Microsoft SharePoint Server tilviksins sem verður að vera skilgreind fyrir þess háttar málefni. Nánari upplýsingar, sjá [Nota Rafræna skýrslugerð skilgreiningu til að gefa Power BI með gögnum úr Dynamics 365 Aðgerðir](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Ábending:** til Að hnekkja sjálfgefna hegðun (sem er, svarglugganum fyrir skilgreiningu), er hægt að stofna tilvísun áfangastaðar og áfangastað skrár fyrir aðal frálagsíhlutinn, og óvirkja svo alla áfangastaði.

## <a name="security-considerations"></a>Öryggisatriði
Tvær gerðir af skyldum og réttindum eru notaðar fyrir áfangastaði rafrænnar skýrslugerðar. Eina gerð stjórnar möguleikanum á að viðhalda almennri áfangastaði sem eru skilgreind fyrir lögaðila (sem er það stýrir aðgangi að í **Rafræna skýrslugerð áfangastaði** síðuna). Önnur gerð stjórnar möguleikanum fyrir notanda forrits til að hnekkj, á keyrslutíma, stillingarnar áfangastaðar sem eru skilgreind af forritara rafrænnar skýrslugerðar eða hagnýtur ráðgjafi rafrænnar skýrslugerðar.

| Hlutverk (AOT-heiti)                     | Heiti hlutverks                                  | Skylda (AOT-heiti)                     | Heiti skyldu                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Þróunaraðili rafrænnar skýrslulausnar             | ERFormatDestinationConfigure        | Skilgreina viðtökustað rafræns skýrslugerðarsniðs                |
| ERFunctionalConsultant              | Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar | ERFormatDestinationConfigure        | Skilgreina viðtökustað rafræns skýrslugerðarsniðs                |
| PaymAccountsPayablePaymentsClerk    | Starfsmaður viðskiptaskuldagreiðslna            | ERFormatDestinationRuntimeConfigure | Skilgreina viðtökustað rafræns skýrslugerðarsniðs við keyrslu |
| PaymAccountsReceivablePaymentsClerk | Starfsmaður viðskiptakröfugreiðslna         | ERFormatDestinationRuntimeConfigure | Skilgreina viðtökustað rafræns skýrslugerðarsniðs við keyrslu |

**Athugasemd:** Tvær réttindi eru notuð í fyrri skyldum. Þessi réttindi hafa sama heiti og samsvarandi skyldum: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Algengar spurningar
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Ég hef flutt inn rafræna skilgreiningar og ég sé þær á síðunni fyrir skilgreiningar Rafræna skýrslugerð. En því ekki ég þær á Rafræna skýrslugerð áfangastaði síðu?

Gangið úr skugga um að smellt er á **Nýtt** og veljið síðan skilgreiningu í á **Tilvísun** svæði. Á **áfangastaði Rafræna skýrslugerð ** síðu er hægt að sjá aðeins skilgreiningar sem áfangastaðir hafa verið skilgreind fyrir.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Á hvaða leið til að skilgreina hvaða lykill Azure Geymslu og geymslu Azure Blob notuð?

Nei. Geymsla sjálfgefna Azure Blob sem er skilgreind og er notað fyrir skjalastjórnunarkerfið er notað.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Það er málefni Skrá áfangastaðar í stillingar fyrir áfangastað? Hvað gerir sú stillingu?

**Skrá** áfangastaður er notuð til að stýra svarglugga. Ef þessi áfangastað, eða ef enginn áfangastaður er skilgreind fyrir afbrigði, að sjá og opna eða vista svarglugga eftir upp frálagsskráin er stofnuð.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Er Hægt að veita dæmi um formúluna sem vísar til reikning lánardrottins sem ég get set tölvupóst til?

Athugið að formúlur eru sérstaklega ætlaðar fyrir skilgreiningu rafrænnar skýrslugerðar. Dæmi: Ef ISO 20022 skilgreining millifærslu fjármuna er notuð, **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** eða **líkan. Payments.Creditor.Identification.SourceID** til að fá lykill lánardrottins sem er tengd.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Einn af mínar skilgreiningar sniðs inniheldur margar skrár sem eru flokkaðar í einni möppu (t.d. Folder1 inniheldur File1, File2 og File3). Hvernig set ég upp áfangastaði þannig að Folder1.zip var ekki stofnuð yfir höfuð, File1 er send með tölvupósti, File2 er sent til SharePoint og ég get opnað File3 strax eftir skilgreining eer keyrð?

Skilyrðið er skal snið verður að vera tiltæk í afbrigðum ER. Ef þú ert með sniðið þitt, skal opna sem **áfangastað Rafræn skýrslugerðar ** síðunni og stofna ný tilvísun í þessa skilgreiningu. Síðan verður að hafa fjóra áfangastaði skráa , ein fyrir hvern frálagsíhlut. Stofna fyrsta ákvörðunarstað skrár , gefa því heiti eins og **Möppu**, og veljið skrárnafn sem táknar möppu í þinni skilgreiningu. Smellið á **Stillingar**, og gangið úr skugga um að allar áfangastaði eru óvirkir. Fyrir þessa áfangasta skrár, verður mappan ekki stofnuð. Að sjálfgefnu, vegna tengsla stigveldis milli skrár og yfirskipaðra mappa, munu skrárnar verða hegða sér á sama hátt. Með öðrum orðum þeir ekki verða sendir neitt. Til að hnekkja þeirri sjálfgefinni hegðun, verður að stofna þrjá fleiri áfangastaði skrár , einn fyrir hverja skrá. Í stillingum áfangastaðar fyrir hverja, þarf að virkja ákvörðunarstað sem á að senda skrána á.

# <a name="see-also"></a>Sjá einnig

[Yfirlit yfir Rafræna skýrslugerð](general-electronic-reporting.md)


