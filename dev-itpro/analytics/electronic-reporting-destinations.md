---
title: "Viðtökustaður rafrænnar skýrslugerðar"
description: "Hægt er að skilgreina áfangastað inn fyrir hverja skilgreiningarsnið Rafrænnar skýrslugerðar (ER) og íhlut úttaks þess (möppu eða í skrá). Notendur sem fá viðeigandi aðgangsheimildir geta einnig breytt stillingar fyrir áfangastað á keyrslutíma. Þessi skrá útskýrir áfangastaðastjórnun rafrænnar skýrslugerðar, gerðir áfangastaða sem eru studdar, og öryggisatriði."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5fb008420f82abd7983ee26854f84330705c0c01
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-reporting-destinations"></a>Viðtökustaður rafrænnar skýrslugerðar

[!include[banner](../includes/banner.md)]


Hægt er að skilgreina áfangastað inn fyrir hverja skilgreiningarsnið Rafrænnar skýrslugerðar (ER) og íhlut úttaks þess (möppu eða í skrá). Notendur sem fá viðeigandi aðgangsheimildir geta einnig breytt stillingar fyrir áfangastað á keyrslutíma. Þessi skrá útskýrir áfangastaðastjórnun rafrænnar skýrslugerðar, gerðir áfangastaða sem eru studdar, og öryggisatriði.

Rafræn skýrslugerð (ER) skilgreiningar sniðs innihalda yfirleitt minnst einn frálagsíhlut: skrá. Skilgreiningar innihalda yfirleitt margar frálagsíhluti skráa af mismunandi gerðum (t.d. XML, TXT eða XLSX) sem eru flokkaðar í annað hvort í einni möppu eða margar möppur. Stjórnun áfangastaðar Rafrænnar skýrslugerðar gerir kleift að forstilla hvað gerist þegar hver íhlutur er keyrður. Að sjálfgefnu þegar afbrigði er keyrð, sér notandi svarglugga sem er hægt að nota til að vista eða opna skrána. Sama hegðun er einnig notuð þegar þú flytur inn skilgreiningu rafrænnar skýrslugerðar og skilgreinir ekki tilteknu áfangastaði fyrir hana. Eftir á ákvörðunarstað hefur verið stofnuð fyrir aðal frálagsíhlut, hnekkir sá ákvörðunarstað sjálfgefinni hegðun og möppu eða skráin er send samkvæmt stillingum áfangastaðar.

## <a name="availability-and-general-prerequisites"></a>Framboð og almenn skilyrði
Áfangastaðir rafrænnar skýrslugerðar er ekki tiltæk í útgáfu Microsoft Dynamics 365 for Operations 7.0 (febrúar 2016). Þess vegna verður að setja upp Microsoft Dynamics 365 for Operations (nóvember 2016 útgáfu) til að nota allar aðgerðir sem er lýst í þessu efnisatriði. Einnig er hægt að setja upp einn af eftirfarandi skilyrðum. Hins vegar þarftu að athuga að þessir valkostir veita meira takmarkað rafræna skýrslugerð viðtökustaður upplifun.

-   Microsoft Dynamics 365 fyrir Aðgerðir útgáfu 7.0.1 (maí 2016)
-   Stjórnun áfangastaður fyrir rafræna skýrslugerð [bráðabót forrits](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Hægt er að setja upp áfangastaði aðeins fyrir skilgreiningar rafrænnar skýrslugerðar sem hafa verið fluttar inn, og fyrir sniðin sem eru tiltækir í **skilgreiningar rafrænnar skýrslugerðar** síðu.

## <a name="overview"></a>Yfirliti
Stjórnun áfangastaðar fyrir rafræna skýrslugerð aðgerðir eru tiltækar á **fyrirtækisstjórnun** &gt; **Rafræna skýrslugerð**. Hér er hægt að hnekkja sjálfgefna hegðun fyrir skilgreiningu. Innfluttar skilgreiningar eru ekki sýnd hér fyrr en smellt er á **Nýtt** og síðan, í á **Tilvísun** reit, skal velja skilgreiningu til að stofna stillingar fyrir áfangastað fyrir.

[![Velja skilgreiningu í svæðinu Tilvísun](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Þegar búið er að stofna tilvísun er hægt að stofna áfangastað skrár fyrir hverja möppu eða fyrir skrá. 

[![Stofnun viðtöðustaðar skráar](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Athugið**: hægt er að stofna eina áfangastað fyrir hverja frálagsskrá af sama sniði, eins og möppu eða skrá sem er valin í **skrárnafn** reit. Síðan er hægt að virkja og óvirkja staka áfangastaði fyrir áfangastað skrár aðskilið í **stillingar fyrir Áfangastað** svarglugga. **Stillingar** hnappinn er notuð til að stjórna áfangastaði fyrir valinn áfangastað skrár. Í **stillingar fyrir Áfangastað** svarglugganum er hægt að stjórna hvern ákvörðunarstað sérstaklega með því að stilla **Virkt** valkost fyrir hana.

[![Svargluggi áfangastaðastillinga](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg).

## <a name="destination-types"></a>Gerðir áfangastaða
Ýmsar gerðir áfangastaði eru studd. Þú getur virkjað eða óvirkjað allar gerðir á sama tíma. Á þennan hátt er annað hvort hægt að gera ekkert eða senda íhlutinn á allar skilgreinda áfangastaði. Eftirfarandi kaflar lýsa áfangastaði sem eru studdar.

### <a name="email-destination"></a>Áfangastður tölvupósts

Setja **Virkt** til **Já** til að senda frálagsskrá með tölvupósti. Eftir að þessi valkostur er virkjaður er hægt að breyta efni tölvupósts og tilgreina viðtakendur tölvupósts og meginmál tölvupósts. Hægt er að setja upp fastatexta fyrir efni og meginmál tölvupósts eða hægt er að nota formúlur rafræn skýrslugerð til að gagnvirkt stofna texta tölvupósts. Hægt er að grunnstilla netföng fyrir rafræn skýrslugerð á tvo vegu. Grunnstillingu má ljúka á sama hátt og Prentstýring eiginleiki í Dynamics 365 for Operations lýkur henni. Að öðrum kosti, er hægt að leysa úr netfangi með því að nota beina tilvísun í skilgreiningu rafræn skýrslugerð skilgreining til og með formúla.

### <a name="email-address-types"></a>Gerðir tölvupóstfanga

Þegar smellt er á **Breyta** fyrir **Til** eða **Cc** reitina birtist svarglugginn **Senda tölvupóst til**. Síðan er hægt að velja rétta gerð tölvupóstfangs til að nota.

[![Netfang í svargluggi](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Prentstýring

Ef valið er **Prentstýring tölvupóstur** gerð, geturðu fært inn fast netfang í **Til** svæði. Til að nota tölvupóstföng sem eru ekki föst, verður að velja upprunagerð tölvupósts fyrir áfangastað skrár. Eftirfarandi virði eru studd: **Viðskiptavinur**, **Lánardrottinn**, **Viðfang**, **Tengiliður**, **Samkeppnisaðili**, **Starfskraftur**, **Umsækjandi**, **Væntanlegur lánardrottinn**, og **Lánardrottinn án leyfis**. Eftir að þú velur gerð tölvupóstuppruna skal nota hnappinn áfram í **Upprunareikningur tölvupósts** svæði til að opna **Formúluhönnuður **skjámynd. Hægt er að nota þessa skjámynd til að festa formúla sem stendur fyrir valinn aðilalykil í áfangastað tölvupósts.

[![Grunnstilla Tölvupóstur vegna prentstýringar](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Athugið að formúlur eru við tilgreindar fyrir skilgreiningu rafrænnar skýrslugerðar. Í **formúla**, Færið inn skjalbundna tilvísun í viðskiptavin eða lánardrottinn gerð aðila. Í stað þess að slá inn, hægt að finna gagnaveituhnút sem stendur fyrir lykil viðskiptavinar eða lánardrottins, og smella á **bæta Við gagnaveitu** hnappinn til að uppfæra formúlu. Dæmi: Ef ISO 20022 skilgreining millifærslu fjármuna er notuð, hnúta sem standa fyrir lykil lánardrottins er  **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Annars að færa inn strenggildi, eins og **DE-001**, til að vista formúlu.

[![Formúluhönnuður](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Í **netfang í** svargluggi, er smellt á endurvinnslukörfuna við hliðina á svæði **Upprunareikningur tölvupósts** svæði til að eyða formúlunni endanlega fyrir upprunareikning tölvupósts. Að öðrum kosti, opið formúluhönnuður til að breyta formúlunni sem var áður vistuð. Til að úthluta netföngum er smellt á **Breyta** til að opna **Úthluta netfang** svargluggi.

[![Úthluta netföngum fyrir áfangastað tölvupósts](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Skilgreiningartölvupóstur

Notaðu þessa gerð tölvupósts ef skilgreiningin sem þú notar er með hnút í gagnaveitum sem standa fyrir netfang. Hægt er að nota gagnaveitur og aðgerðir í formúluhönnuður til að ná rétt sniðnu netfang.

[![Úthluta gagnaveitu netfanga fyrir áfangastað tölvupósts](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Athugasemd:** SMTP-samskiptareglur (SMTP) þjóns verða að vera skilgreindar og tiltækar. Hægt er að tilgreina smtp-þjónninn í Dynamics 365 for Operations við **kerfisstjórnun** &gt; **Uppsetningu**&gt;**Tölvupósti** &gt; **færibreytur Tölvupósts**.

### <a name="archive-destination"></a>áfangastaður skjalasafns

Hægt er að nota þennan valkost til að senda frálag annað hvort á Microsoft SharePoint-möppu eða Microsoft Azure Geymslu. Stilla **Virkt** á **Já** til að senda frálag á áfangastað sem er skilgreind með völdu skjalagerðina. einungis gerð skjals þar sem flokksins er stillt á **Skrá** eru tiltækar til vals. Hægt er að Skilgreina gerðir skjala í **fyrirtækisstjórnun** &gt; **Skjalastjórnun** &gt; **Skjalagerðir**. Skilgreining fyrir áfangastaði rafrænnar skýrslugerðar er sú sama og skilgreiningin fyrir skjalastjórnunarkerfið.

[![Síðan Gerðir skjala](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Staðsetning ákvarðar hvar skráin er vistuð. Eftir að áfangastaður **skjalasafns** er virkjaður er hægt að vista niðurstöður skilgreiningarframkvæmdar í Vinnsla skjalasafn. Hægt er að skoða niðurstöðurnar í **Fyrirtækisstjórnun** &gt; **Rafræn skýrslugerð** &gt; **Viðtökustaður rafrænnar skýrslugerðar**. **athugasemd:** Hægt er að velja gerð skjals fyrir Vinnsla skjalasafns í Dynamics 365 for Operations, í **Fyrirtækisstjórnun** &gt; **Vinnusvæði** &gt; **Rafræn skýrslugerð** &gt; **Rafræn skýrslugerð færibreytur**.

#### <a name="sharepoint"></a>SharePoint

Hægt er að vista skrá í möppu merktu SharePoint. Hægt er að Tilgreina sjálfgefinn þjón SharePoint á **fyrirtækisstjórnun** &gt; **Skjalastjórnun** &gt; **Færibreytur skjalastjórnunar**á í **SharePoint** flipanum. Eftir að SharePoint-möppu er skilgreint er hægt að velja það sem möppu þar sem frálag rafrænnar skýrslugerðar verður vistuð fyrir skráargerðina. 

[![Val á SharePoint-möppu](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure-geymsla

Þegar staðsetning gerðar skjals er stillt á **skjalasafn**, er hægt að vista skrá í Azure Geymslu.

### <a name="file-destination"></a>Viðtökustaður skráar

Ef **Virkt** er stillt á **Já** birtist opinn eða vistaður svargluggi þegar skilgreiningin hefur klárað keyrsluna.

### <a name="screen-destination"></a>Áfangastaður skjás

Ef **Virkt** er stillt á **Já**, er forskoðun á frálagi stofnuð. Hægt er að skoða sumar skáargerðir, t.d. XML, TXT, eða .PDF, dirbeint í glugga vafrans. Fyrir aðrar skráargerðir eins og Microsoft Excel eða Word er þjónustan Microsoft Office Online notuð.

### <a name="power-bi-destination"></a>Áfangastaður Power BI

Stilltu **Virkt** á **Já** til að nota skilgreiningu Rafræna skýrslugerðar til að sjá um flutning gagna úr tilviki Dynamics 365 for Operations til Microsoft Power BI-þjónustu. Fluttar skrárnar eru vistaðar í tilviki Microsoft SharePoint Server sem verður að vera skilgreint fyrir þess háttar tilgang. Nánari upplýsingar má nálgast á [Nota skilgreiningu Rafræna skýrslugerð til að gefa Power BI gögnum úr Dynamics 365 for Operations](general-electronic-reporting-report-configuration-get-data-powerbi.md) **Ábending:** til Að hnekkja sjálfgefna hegðun (sem er, svarglugganum fyrir skilgreiningu), er hægt að stofna tilvísun áfangastaðar og áfangastað skrár fyrir aðal frálagsíhlutinn, og óvirkja svo alla áfangastaði.

## <a name="security-considerations"></a>Öryggisatriði
Tvær gerðir af skyldum og réttindum eru notaðar fyrir áfangastaði rafrænnar skýrslugerðar. Ein gerð stjórnar möguleikanum á að viðhalda almennum áfangastaði sem eru skilgreind fyrir lögaðila (það er, hún stjórnar aðgangi að **áfangastöðum rafrænnar skýrslugerðar** síðu). Önnur gerð stjórnar möguleikanum fyrir notanda forrits til að hnekkj, á keyrslutíma, stillingarnar áfangastaðar sem eru skilgreind af forritara rafrænnar skýrslugerðar eða hagnýtur ráðgjafi rafrænnar skýrslugerðar.

| Hlutverk (AOT-heiti)                     | Heiti hlutverks                                  | Skylda (AOT-heiti)                     | Heiti skyldu                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Þróunaraðili rafrænnar skýrslulausnar             | ERFormatDestinationConfigure        | Skilgreina viðtökustað rafræns skýrslugerðarsniðs                |
| ERFunctionalConsultant              | Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar | ERFormatDestinationConfigure        | Skilgreina viðtökustað rafræns skýrslugerðarsniðs                |
| PaymAccountsPayablePaymentsClerk    | Starfsmaður viðskiptaskuldagreiðslna            | ERFormatDestinationRuntimeConfigure | Skilgreina viðtökustað rafræns skýrslugerðarsniðs við keyrslu |
| PaymAccountsReceivablePaymentsClerk | Starfsmaður viðskiptakröfugreiðslna         | ERFormatDestinationRuntimeConfigure | Skilgreina viðtökustað rafræns skýrslugerðarsniðs við keyrslu |

**Athugasemd:** Tvær réttindi eru notuð í fyrri skyldum. Þessi réttindi hafa sama heiti og samsvarandi skyldum: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Algengar spurningar
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Ég hef flutt inn rafræna skilgreiningar og ég sé þær á síðunni fyrir skilgreiningar Rafræna skýrslugerð. En af hverju sé ég ekki þær á síðu fyrir áfangastaði Rafrænnar skýrslugerðar?

Gangið úr skugga um að smellt er á **Nýtt** og veldu síðan skilgreiningu í á **Tilvísun** svæði. Á **áfangastaði Rafræna skýrslugerð** síðu er hægt að sjá aðeins skilgreiningar sem áfangastaðir hafa verið skilgreind fyrir.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Er einhver leið til að skilgreina hvaða Azure Geymslulykil og Azure Blob geymsla er notaður?

Nei. Sjálfgefna Azure Blob geymslan sem er skilgreind og notað fyrir skjalastjórnunarkerfið er notað.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hver er tilgangur áfangastaðar skrár í stillingar fyrir áfangastað? Hvað gerir sú stillingu?

**Skrá** áfangastaður er notuð til að stýra svarglugga. Ef þessi áfangastað er virkjaður, eða ef enginn áfangastaður er skilgreind fyrir skilgreiningu, sést opinn eða vistaður svargluggi eftir að frálagsskráin er stofnuð.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Er Hægt að veita dæmi um formúluna sem vísar til reikning lánardrottins sem ég get set tölvupóst til?

Athugið að formúlur eru sérstaklega ætlaðar fyrir skilgreiningu rafrænnar skýrslugerðar. Dæmi: Ef ISO 20022 skilgreining millifærslu fjármuna er notuð, **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** eða **líkan. Payments.Creditor.Identification.SourceID** til að fá lykill lánardrottins sem er tengd.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Einn af mínar skilgreiningar sniðs inniheldur margar skrár sem eru flokkaðar í einni möppu (t.d. Folder1 inniheldur File1, File2 og File3). Hvernig set ég upp áfangastaði þannig að Folder1.zip var ekki stofnuð yfir höfuð, File1 er send með tölvupósti, File2 er sent til SharePoint og ég get opnað File3 strax eftir skilgreining eer keyrð?

Skilyrðið er skal snið verður að vera tiltæk í skilgreiningum rafrænnar skýrslugerðar. Ef þú ert með sniðið þitt, skal opna sem **áfangastað Rafræn skýrslugerðar** síðunni og stofna ný tilvísun í þessa skilgreiningu. Síðan verður að hafa fjóra áfangastaði skráa , ein fyrir hvern frálagsíhlut. Stofna fyrsta ákvörðunarstað skrár , gefa því heiti eins og **Möppu**, og veljið skrárnafn sem táknar möppu í þinni skilgreiningu. Smellið á **Stillingar**, og gangið úr skugga um að allar áfangastaði eru óvirkir. Fyrir þessa áfangasta skrár, verður mappan ekki stofnuð. Að sjálfgefnu, vegna tengsla stigveldis milli skrár og yfirskipaðra mappa, munu skrárnar verða hegða sér á sama hátt. Með öðrum orðum þeir ekki verða sendir neitt. Til að hnekkja þeirri sjálfgefinni hegðun, verður að stofna þrjá fleiri áfangastaði skrár , einn fyrir hverja skrá. Í stillingum áfangastaðar fyrir hverja, þarf að virkja ákvörðunarstað sem á að senda skrána á.

# <a name="see-also"></a>Sjá einnig

[Yfirlit yfir Rafræna skýrslugerð](general-electronic-reporting.md)




