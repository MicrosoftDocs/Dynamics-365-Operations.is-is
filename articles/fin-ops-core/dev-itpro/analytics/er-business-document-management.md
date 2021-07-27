---
title: Yfirlit yfir stjórnun viðskiptaskjala
description: Þetta efni veitir upplýsingar um hvernig á að nota viðskiptaskjalastjórnunaraðgerð ER-ramma.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bc6363a96d87bf280a34dda34533bc71e21eb6b2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344931"
---
# <a name="business-document-management-overview"></a>Yfirlit yfir stjórnun viðskiptaskjala

[!include [banner](../includes/banner.md)]

Fyrirtækjanotendur nota ramma [Rafrænnar skýrslugerðar (ER)](general-electronic-reporting.md) til að skilgreina snið fyrir skjöl á útleið í samræmi við lagaskilyrði mismunandi landa/svæða. Notendur geta einnig skilgreint gagnaflæðið til að tilgreina hvaða forritsgögn eru sett í skjöl sem eru búin til. ER-ramminn býr til skjöl á útleið í Microsoft Office-sniðum (Excel-vinnubækur eða Word-skjöl) með því að nota fyrirframskilgreind sniðmát. Sniðmátin eru fyllt út með tilskildum gögnum í samræmi við stillanlegt gagnaflæði meðan nauðsynleg skjöl eru búin til. Hægt er að birta hvert skilgreint snið sem hluta af ER lausn til að búa til sérstök skjöl á útleið. Þetta er táknað með ER sniði sem getur innihaldið sniðmát sem þú getur notað til að búa til mismunandi skjöl á útleið. Fyrirtækjanotendur geta notað þennan ramma til að stjórna nauðsynlegum viðskiptaskjölum.

**Stjórnun viðskiptaskjala** er smíðað ofan á ramma rafrænnar skýrslugerðar og gerir fyrirtækjanotendum kleift að breyta sniðmátum viðskiptaskjala með því að nota þjónustu Microsoft 365 eða viðeigandi Microsoft Office-skjáborðsforrit. Breytingar á skjölunum gætu falist í því að breyta hönnun viðskiptaskjala og bæta við staðgenglum fyrir viðbótargögn án breytinga á frumkóða og nýjum uppsetningum. Engin vitneskja um ramma ER er nauðsynleg til að uppfæra sniðmát viðskiptaskjala.

> [!NOTE]
> Hafðu í huga að stjórnun viðskiptaskjala gerir þér kleift að breyta sniðmátum sem eru notuð til að framleiða viðskiptaskjöl eins og pantanir, reikninga osfrv. Þó að sniðmáti hafi verið breytt og ný útgáfa af því hafi verið gefin út er þessi útgáfa notuð til að búa til nauðsynleg viðskiptaskjöl. Ekki er hægt að nota stjórnun viðskiptaskjala til að breyta þegar mynduðum viðskiptaskjölum.

## <a name="supported-deployments"></a>Studdar uppsetninar

Sem stendur er viðskiptaskjalastjórnunaraðgerðin aðeins útfærð fyrir skýjauppsetningu. Ef þessi eiginleiki er mikilvægur fyrir uppsetningu þína á staðnum skaltu láta okkur vita með því að veita svörun á svæðinu [Hugmyndir](https://experience.dynamics.com/ideas/).

## <a name="supported-microsoft-office-applications"></a>Studd Microsoft Office forrit

Til að nota viðskiptaskjalastjórnun til að breyta sniðmátum á Excel- eða Word-sniði með því að nota Microsoft Office-skjáborðsforrit verður þú að vera með Microsoft Office 2010 eða nýrra sett upp. Þetta er stutt í uppsetningum í skýi og á staðnum.

Til að nota viðskiptaskjalastjórnun fyrir breytingar á sniðmátum á Excel- eða Word-sniði með því að nota forrit Microsoft 365, þarf að vera með Microsoft 365 Office fyrir vefáskriftina. Þetta er stutt í skýjauppsetningu.

## <a name="business-document-availability"></a>Framboð á viðskiptaskjölum

Fyrir heildarlista yfir allar skýrslur sem áætlaðar eru fyrir október 2019 útgáfuna skal skoða [Skilgreinanleg skýrslugerð viðskiptaskjala í Word og Excel](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

Fyrir heildarlista yfir allar skýrslur sem áætlaðar eru fyrir október 2020 útgáfuna skal skoða [Skilgreinanleg viðskiptaskjöl – Word-sniðmát](/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Fleiri skýrslur verða í boði í síðari útgáfum. Sérstakar tilkynningar um viðbótarskýrslur verða sendar sérstaklega. Frekari upplýsingar um hvernig á að fara yfir lista yfir skýrslur sem eru í boði er að finna í kaflanum [Listi yfir skilgreiningar rafrænnar skýrslugerðar sem hafa verið gefnar út í Finance til að styðja skilgreinanleg viðskiptaskjöl](#list-of-configurations-cbd) hér að neðan.

Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka dæminu í þessu efni.

## <a name="configure-er-parameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar

Þar sem stjórnun viðskiptaskjala er byggð ofan á ER ramma verður þú að stilla ER-færibreytur til að fara að vinna með stjórnun viðskiptaskjala. Til að gera þetta þarftu að setja upp ER-færibreytur eins og lýst er í [Skilgreina ramma rafrænnar skýrslugerðar (ER)](electronic-reporting-er-configure-parameters.md). Þú þarft einnig að bæta við nýjum skilgreiningum sem lýst er í [Stofna skilgreiningarveitendur og merkja þá sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-vinnusvæði.](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Flytja inn ER-lausnir

Dæmi um ER-stillingar eru notaðar í dæminu um þetta ferli. Þú verður að flytja inn í núverandi tilvik af Dynamics 365 Finance, ER stillingar sem innihalda viðskiptaskjalasniðmát sem hægt er að breyta með því að nota viðskiptaskjalastjórnun. Hladdu niður og geymdu síðan eftirfarandi skrár til að ljúka þessu ferli.

**Dæmi um reikningslausn viðskiptavina í ER**

| Skrá                                      | Efni |
|-------------------------------------------|---------|
| Customer invoicing model.version.2.xml    | [Skilgreining á gagnalíkani í ER](https://download.microsoft.com/download/b/f/a/bfa5cb52-e6e2-42bc-a4c0-77014a4c54e6/Customerinvoicingmodel.version.2.xml) |
| Customer FTI report (GER).version.2.3.xml | [Sniðskilgreiningar fyrir frjálsan texta í ER](https://download.microsoft.com/download/3/c/2/3c2e58f2-6e56-43d9-85ea-4c97252a108d/CustomerFTIreportGER.version.2.3.xml) |

**Dæmi um ávísanalausn í ER**

| Skrá                                     | Efni |
|------------------------------------------|---------|
| Model for cheques.version.10.xml         | [Skilgreining á gagnalíkani í ER](https://download.microsoft.com/download/3/7/6/376cb0f6-181a-4895-a432-390ffca64162/Modelforcheques.version.10.xml) |
| Cheques printing format.version.10.9.xml | [Skilgreining ávísanasniðs í ER](https://download.microsoft.com/download/6/d/6/6d61bfff-3d89-4377-9e34-2e3ee6d6df91/Chequesprintingformat.version.10.9.xml) |

**Dæmi um lausn fyrir erlend viðskipti í ER**

| Skrá                             | Efni |
|----------------------------------|---------|
| Intrastat model.version.1.xml    | [Skilgreining á gagnalíkani í ER](https://download.microsoft.com/download/2/0/0/200d6ed1-eff8-48ec-ab75-175a4acf9714/Intrastatmodel.version.1.xml) |
| Intrastat report.version.1.9.xml | [Skilgreiningar fyrir snið Intrastat-eftirlitsskýrslu í ER](https://download.microsoft.com/download/7/a/2/7a2a27c3-a8a5-42a1-9d04-f0a8e1ec1707/Intrastatreport.version.1.9.xml) |

Notaðu eftirfarandi ferli til að flytja inn hverja skrá. Flyttu inn skilgreiningar *gagnalíkans* í ER fyrir hverja ER-lausn í töflunum hér að ofan áður en þú flytur inn samsvarandi skilgreiningu á *sniði* í ER.

1. Opnaðu síðuna **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Efst á síðunni velurðu **Gengi**.
3. Veldu **Hlaða úr XML-skrá**.
4. Veldu **Fletta** til að hlaða umbeðinni XML-skrá.
5. Veldu **Í lagi** til að staðfesta innflutning á skilgreiningum.

![Skilgreiningarsíða rafrænnar skýrslugerðar staðfestir innflutning skilgreiningar.](./media/BDM-Overview-ERSolutions.png)

Einnig er hægt að flytja opinberlega út ER-snið stillingar frá Microsoft Dynamics Lifecycle Service (LCS). Til dæmis, til að ljúka þessari aðferð, getur þú flutt inn nýjustu útgáfuna af **Ókeypis textareikningur (Excel)** skilgreiningu ER sniðs. Samsvarandi ER gagnalíkan og skilgreiningar ER-líkanavörpunar verða fluttar inn sjálfkrafa.

![Efnissíða fyrir samnýtt eignasafn LCS.](./media/BDM-Overview-SharedAssetLibrary.png)

Nánari upplýsingar um innflutning ER-skilgreininga er að finna í [Stjórna líftíma ER-stillinga](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Virkja stjórnun viðskiptaskjala

Til að hefja stjórnun viðskiptaskjala þarftu að opna vinnusvæðið **Stjórnun eiginleika** og virkja eiginleikann **Stjórnun viðskiptaskjala**.

Notaðu eftirfarandi ferli til að virkja virknina Stjórnun viðskiptaskjala fyrir alla lögaðila.

1. Opnaðu vinnusvæðið **Eiginleikastjórnun**.
2. Á flipanum **Nýtt** velurðu aðgerðina **Stjórnun viðskiptaskjala** á listanum.
3. Veldu **Virkja núna** til að kveikja á völdum eiginleika.
4. Endurnýjaðu síðuna til að fá aðgang að nýja eiginleikanum.

> [!NOTE]
> Nánari upplýsingar um notkun nýja skjal notendaviðmótsins í viðskiptaskjalastjórnun, sjá [Nýtt notendaviðmót skjala í viðskiptaskjalastjórnun](er-business-document-management-new-template-ui.md).

![Vinnusvæði eiginleikastjórnunar.](./media/BDM-Overview-FMEnabling.png)

Nánari upplýsingar um að virkjun nýrra eiginleika er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Skilgreina færibreytur

Notaðu upplýsingarnar í eftirfarandi hlutum til að setja upp grunnfæribreytur fyrir stjórnun viðskiptaskjala.

### <a name="prerequisites-for-parameter-setup"></a>Forsendur fyrir uppsetningu á færibreytum

Áður en þú getur sett upp stjórnun viðskiptaskjala verður þú að setja upp nauðsynlega skjalagerð í skjalastjórnunarramma. Þessi skjalagerð er notuð til að tilgreina tímabundna geymslu skjala á Office-sniðum (Excel og Word) sem eru notuð sem sniðmát fyrir ER-skýrslur. Hægt er að breyta sniðmáti tímabundnar geymslu með því að nota Office-skjáborðsforritin.

Fyrir þessa skjalagerð verður að velja eftirfarandi eigindagildi.

| Heiti eigindar | Eigindargildi |
|----------------|-----------------|
| Klasi          | Tengja skrá     |
| Hópur          | Skrá            |
| Staðsetning       | SharePoint      |

Fyrir upplýsingar um hvernig á að setja upp nauðsynlegar færibreytur fyrir skjalastjórnun og skjalagerðir skal sjá [Skilgreina skjalastjórnun](../../fin-ops/organization-administration/configure-document-management.md).

![Setja upp skjalagerð í skjalastjórnun.](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Setja upp færibreytur

Hægt er að setja upp grunnfæribreytur fyrir viðskipti skjal á síðunni **Færibreytur viðskiptaskjala**. Aðeins tilteknir notendur geta nálgast síðuna. Þar á meðal eru:

- Notendur sem er úthlutað á hlutverkið **Kerfisstjóri**.
- Notendur sem er úthlutað í hlutverk sem er skilgreint til að gegna skyldunni, **Hafa umsjón með færibreytum viðskiptaskjalastjórnunar** (AOT heiti **ERBDMaintainParameters**).

Notaðu eftirfarandi ferli til að setja upp grunnfæribreytur fyrir alla lögaðila.

1. Skráðu þig inn sem notandi með aðgang að síðunni **Færibreytur viðskiptaskjala**.
2. Farðu í **Samtök stjórnsýslu** \> **Rafræn skýrslugerð** \> **Stjórnun viðskiptaskjala** \> **Færibreytur viðskiptaskjala**.
3. Á síðunni **Færibreytur viðskiptaskjala**, á flipanum **Viðhengi**, í reitnum **SharePoint skjalagerð** skaltu skilgreina gerð skjalsins sem á að nota til að geyma sniðmát tímabundið á Office-sniðum meðan þeim er breytt með Office-skjáborðsforritunum. 

> [!NOTE]
> Aðeins skjalategundir sem eru stilltar með SharePoint-staðsetningu eru tiltækar fyrir þessa færibreytu.

![Settu upp færibreytur viðskiptaskjalastjórnunar.](./media/BDM-Overview-BDMSetting.png)

Valin skjalategund er fyrirtækjasértæk og verður notuð þegar notandinn er að vinna með viðskiptaskjalastjórnun í fyrirtækinu sem valin skjalategund er skilgreind fyrir. Þegar notandinn er að vinna með viðskiptaskjalastjórnun í öðru fyrirtæki, verður sama valda skjalategund notuð ef skjalategund hefur ekki verið skilgreind fyrir fyrirtækið. Þegar gerð skjals hefur verið skilreind verður hún notuð í stað þeirrar sem var valin í reitnum **SharePoint-skjalagerð**.

> [!NOTE]
> Færibreytan **SharePoint-skjalagerðar** skilgreinir SharePoint-möppu sem tímabundna geymslu fyrir sniðmát sem hægt er að breyta með annaðhvort Microsoft Excel eða Word. Þú verður að setja þessa færibreytu upp ef þú ætlar að nota þessi Office skrifborðsforrit til að breyta sniðmátum. Fyrir frekari upplýsingar, sjá [Breyta sniðmáti í Office skrifborðsforritinu](#EditInOfficeDesktopApp). Hægt er að hafa þessa færibreytu auða ef ætlunin er að breyta sniðmátinu með því að nota aðeins virknina í Microsoft 365. Frekari upplýsingar er að finna í [Breyta sniðmáti í Microsoft 365](#EditInOffice365).

## <a name="configure-access-permissions"></a>Skilgreina aðgangsheimildir

Sjálfgefið er að þegar aðgangur að heimildum fyrir viðskiptaskjalastjórnun er ekki virkur mun sérhver notandi sem hefur aðgang að vinnusviði viðskiptaskjalastjórnunar sjá öll ER-lausnasniðmát sem eru fáanleg. Vinnusvæðið Stjórnun viðskiptaskjala mun aðeins sýna þau sniðmát sem búa í skilgreiningum á ER-sniði og eru merkt með merkinu **Gerð viðskiptaskjala**.

![Skilgreiningarsíða rafrænnar skýrslugerðar með merki viðskiptaskjalagerðar.](./media/BDM-Overview-ERFormatTags.png)

Hægt er að takmarka listann yfir sniðmát í vinnusvæðinu Stjórnun viðskiptaskjala með því að skilgreina aðgangsheimildir. Þetta getur verið mikilvægt þegar mismunandi sniðmát eru notuð til að mynda viðskiptaskjöl fyrir mismunandi viðskiptalén (rekstrarsvið) og þú vilt leyfa sérstökum notendum aðgang að mismunandi sniðmátum til að breyta í vinnusvæðinu Stjórnun viðskiptaskjala.

Hægt er að stilla aðgangsheimildir stjórnunar viðskiptaskjala í **Stillingar fyrir aðgangsheimildir**. Aðeins eftirfarandi notendur geta nálgast síðuna:

- Notendur sem er úthlutað á hlutverkið **Kerfisstjóri**.
- Notendur sem úthlutað er á öll önnur hlutverk sem eru skilgreind til að gegna skyldunni, **Skilgreina aðgangsheimildir að sniðmátum viðskiptaskjala til að gera breytingar** (AOT-heiti **ERBDTemplates Security**).

Notaðu eftirfarandi ferli til að setja upp aðgangsheimildir fyrir Stjórnun viðskiptaskjala fyrir alla lögaðila.

1. Skráðu þig inn sem notandi með aðgang að síðunni **Stillingar fyrir aðgangsheimildir**.
2. Farðu í **Samtök stjórnsýslu** \> **Rafræn skýrslugerð** \> **Stjórnun viðskiptaskjala** \> **Stjórna aðgangsheimildum**.

    Athugaðu tilkynninguna sem upplýsir þig um að notkun aðgangsheimilda fyrir stjórnun viðskiptakjala sé ekki virkjuð sem stendur.

    ![Síðan Stillingar aðgangsheimilda stjórnunar viðskiptaskjala.](./media/BDM-Overview-TemplatesAccess1.png)

    Með þessari stillingu er geta allir notendur sem er úthlutað á öryggishlutverk sem er skilgreint til að framkvæma skylduna **Stjórna sniðmátum viðskiptaskjala** (AOT-heiti **ERBDManageTemplates**) opnað vinnusvæðið Stjórnun viðskiptaskjala og breytt öllum sniðmátum sem eru í boði.

    Eftirfarandi mynd sýnir það sem er í boði á vinnusvæðinu Stjórnun viðskiptaskjala fyrir notendur sem úthlutað er á hlutverkið **Starfsmaður viðskiptakrafa**. Með núverandi stillingu aðgangsheimilda getur notandinn breytt sniðmátum viðskiptaskjala úr mismunandi starfssvæðum, þar með talið reikningum, lögboðnum skýrslum og greiðslum.

    ![Vinnusvæðasíða viðskiptaskjalastjórnunar fyrir starfsmann viðskiptakrafna.](./media/BDM-Overview-TemplatesForAlice1.png)

3. Á síðunni **Stillingar fyrir aðgangsheimildir** velurðu **Stillingar aðgangsheimilda**.
4. Í valmyndinni **Stillingar aðgangsheimilda til að breyta sniðmátum** skaltu virkja valkostinn **Nota skilgreindar aðgangsheimildir**.
5. Veldu **Í lagi** til að staðfesta að aðgangsheimildir stjórnunar viðskiptaskjala hafi verið gerðar virkar.

    ![Staðfesta aðgangsheimildir viðskiptaskjalastjórnunar.](./media/BDM-Overview-TemplatesAccess2.png)

6. Veldu **Bæta við** til að slá inn nýtt viðskiptahlutverk sem stilla þarf heimildir fyrir til að fá aðgang að sniðmátum stjórnunar viðskiptaskjala.
7. Í valmyndinni **Öryggishlutverk** velurðu hlutverkið **Starfsmaður viðskiptakrafa** og síðan **Í lagi** til að staðfesta hlutverkavalið.
8. Á flipanum **Aðgangsheimildir fyrir hvert merki stillinga** velurðu **Nýtt**.
9. Í reitnum **Gerð merkis** velurðu **Rekstrarsvæði** og í reitnum **Auðkenni** velurðu **Reikningsfærsla**.
10. Veldu **Vista** til að geyma skilgreindar aðgangsheimildir fyrir valið hlutverk.

    Núverandi stilling þýðir að fyrir hvern notanda sem er úthlutað á hlutverkið **Starfsmaður viðskiptakrafa** og gegnir skyldunni, **Stjórna sniðmátum viðskiptaskjala** (AOT-heiti **ERBDManageTemplates**) verða skilgreiningarsnið ER-sniða sem hafa gildið **Reikningsfærsla** fyrir merkið **Rekstrarsvæði** tiltæk til breytinga í vinnusvæði stjórnunar viðskiptaskjala.

11. Skiptu um rúðuna **Tengdar upplýsingar** frá hægri hlið þessarar síðu. Glugginn **Tengdar upplýsingar** sýnir hvernig skilgreindu aðgangsheimildunum verður beitt, þar með talið hvaða ER-skilgreininarsniðmát verða tiltæk fyrir notendur sem er úthlutað á hlutverkið **Starfsmaður viðskiptakrafa**.

    ![Gluggi tengdra upplýsinga á stillingarsíðu aðgangsheimilda.](./media/BDM-Overview-TemplatesAccess3.png)

12. Á flipanum **Aðgangsheimildir fyrir hvert merki stillinga** velurðu valkostinn **Bæta við**.
13. Í valmyndinni **Velja skilgreiningu** skaltu merkja við skilgreiningu ER-sniðs **Intrastat-skýrsla**.
14. Veldu **Í lagi** til að staðfesta færslu valinna stillinga og veldu síðan **Vista** til að geyma skilgreindar aðgangsheimildir fyrir valið hlutverk.

Núverandi stilling þýðir að fyrir hvern notanda sem er úthlutað á hlutverkið **Starfsmaður viðskiptakrafa** og gegnir skyldunni **Stjórna sniðmátum viðskiptaskjala** (AOT-heiti **ERBDManageTemplates**) verða eftirfarandi sniðmát tiltæk til breytinga í vinnusvæði stjórnunar viðskiptaskjala:

- Sniðmát sem hafa gildið **Reikningsfærsla** fyrir merkið **Rekstrarsvið**.
- Sniðmát úr skilgreiningum ER-sniðs sem skráð eru á flipanum **Aðgangsheimildir eftir skilgreiningum** (sniðmát úr sniðmátsskilgreiningum **Intrastat-skýrslu** í léninu **Lögboðin skýrslugerð** í þessu dæmi).

![Flýtiflipi aðgangsheimilda á stillingarsíðu aðgangsheimilda.](./media/BDM-Overview-TemplatesAccess4.png)

Eftirfarandi mynd sýnir það sem vinnusvæðið Stjórnun viðskiptaskjala veitir notenda sem úthlutað er á hlutverkið **Starfsmaður viðskiptakrafa**. Með núverandi stillingum fyrir aðgangsheimildir fyrir stjórnun viðskiptaskjala getur notandinn breytt sniðmáti viðskiptaskjala úr léninu **Reikningsfærsla** og ER-sniðmátsskilgreiningu **Intrastat-skýrslu**. Sniðmát úr léninu **Greiðslur** eru ekki aðgengileg fyrir hlutverkið **Starfsmaður viðskiptakrafa**.

![Sniðmátum viðskiptaskjala breytt á vinnusvæðasíðu viðskiptaskjalastjórnunar.](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> Reglurnar **Aðgangsheimildir eftir skilgreiningum** eru geymdar með því að nota einkvæmt auðkenni skingreiningar á ER-sniði. Þetta þýðir að þessum reglum verður ekki eytt þegar ER-skilgreiningu sem vísar til þeirra er eytt. Þegar þú flytur aftur inn eyddar skilgreiningar í þetta tilvik munu þessar reglur vísa aftur til þeirra. Það er engin þörf á að setja upp reglurnar aftur eftir að eyddar skilgreiningar hafa verið fluttar aftur inn.

## <a name="use-business-document-management-to-edit-templates"></a>Nota Stjórnun viðskiptaskjala til að breyta sniðmátum

Fyrirtækjanotendur geta nálgast sniðmát viðskiptaskjala til að breyta þeim á vinnusvæði Stjórnunar viðskiptaskjala. Aðeins eftirfarandi notendur hafa aðgang að vinnusvæði viðskiptaskjala:

- Notendur sem er úthlutað á hlutverkið **Kerfisstjóri**.
- Notendur sem er úthlutað í hlutverk sem er skilgreint til að gegna skyldunni, **Stjórna sniðmátum viðskiptaskjala** (AOT-heiti **ERBDManageTemplates**).

Notaðu eftirfarandi ferli til að breyta sniðmátum frjáls texta í vinnusvæði Stjórnunar viðskiptaskjala. Áður en þú lýkur þessu ferli verður þú að hafa lokið öllum fyrri ferlum um þetta efni.

1. Skráðu þig inn sem notandi með aðgang að vinnusvæðinu Stjórnun viðskiptaskjala.
2. Opnaðu vinnusvæðið Stjórnun viðskiptaskjala.

Þegar slökkt er á eigineikanum **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á vinnusvæðinu **Eiginleikastjórnun** sýnir aðalhnitanetið á vinnusvæðinu **Stjórnun viðskiptaskjala** eftirfarandi sniðmát:

- Sniðmát sem eru í eigu ER stillingaveitanda þíns (það er, veitandinn sem nú er merktur sem virkur á vinnusvæðinu **Rafræn skýrslugerð**). Þegar þú hefur valið eitt af þessum sniðmátum geturðu valið **Breyta sniðmáti** til að byrja eða halda áfram að breyta því.
- Sniðmát sem eru í eigu annarra veitenda ER-stillinga. Þegar þú hefur valið eitt af þessum sniðmátum geturðu valið **Nýtt skjal** til að búa til afrit af því sem er í eigu veitanda ER-stillinganna og byrja síðan að breyta afritinu.

![Sniðmátslistar á vinnusvæðasíðu viðskiptaskjalastjórnunar.](./media/BDM-Overview-EditingTemplate1.png)

Flipinn **Sniðmát** sýnir innihald valins sniðmáts. Veldu flipann **Upplýsingar** til að skoða upplýsingar um valið sniðmát sem og upplýsingar um skilgreiningu ER-sniðs sem þetta sniðmát er í. Taktu eftir að öll sniðmátin eru með stöðuna **Birt** og innihalda engar upplýsingar í dálknum **Endurskoðun**. Þetta þýðir að ekki er verið að breyta þessum sniðmátum eins og er.

Þegar kveikt er á eiginleikanum **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á vinnusvæðinu **Eiginleikastjórnun** sýnir aðalnetið á vinnusvæðinu **Stjórnun viðskiptaskjala** sýnir sniðmát sem eru í eigu veitanda ER-stillinganna (það er veitandinn sem nú er merktur sem virkur á vinnusvæðinu **Rafræn skýrslugerð**). Þegar þú hefur valið eitt af þessum sniðmátum geturðu valið **Breyta sniðmáti** til að byrja eða halda áfram að breyta því.

Til að vinna með sniðmát sem eru í eigu annarra veitenda ER-stillinga velurðu **Nýtt skjal** til að búa til afrit af sniðmátinu sem er í eigu ER þjónustuveitunnar. Síðan er hægt að hefja breytingar á afritinu. Nánari upplýsingar er að finna í [Nýtt notandaviðmót fyrir skjöl í stjórnun viðskiptaskjala](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Byrjaðu að breyta sniðmátum í eigu veitanda skilgreiningarinnar

1. Í vinnusvæðinu Stjórnun viðskiptaskjala skaltu velja sniðmátið **Prentsnið ávísana** af listanum.
2. Velja flipann **Upplýsingar**.

![Vinnusvæðasíða viðskiptaskjalastjórnunar, upplýsingaflipi.](./media/BDM-Overview-EditingTemplate2.png)

Valkosturinn **Breyta sniðmáti** er í boði fyrir valið sniðmát. Þessi valkostur er alltaf tiltækur fyrir sniðmát í ER-sniðskilgreiningu sem er í eigu virks veitanda ER-skilgreiningar (**Litware, Inc.** í þessu dæmi). Þegar **Breyta sniðmáti** er valið verður fyrirliggjandi sniðmát úr drögum að útgáfu undirliggjandi ER-sniðskilgreiningar tiltækt til breytinga.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Byrjaðu að breyta sniðmátum í eigu annarra veitenda

1. Veldu vinnusvæðið fyrir viðskipti skjalastjórnunar og veldu skjalið sem þú vilt nota sem sniðmát.

    ![Velja skjal á vinnusvæðasíðu viðskiptaskjalastjórnunar.](./media/BDM-Overview-EditingTemplate3.png)

2. Veldu **Nýtt skjal** og í reitnum **Titill** breytirðu titlinum á breytanlegu sniðmáti ef þörf krefur. Textinn verður notaður til að nefna skilgreiningu ER-sniðsins sem er sjálfkrafa búin til. Athugaðu að drög að þessari skilgreiningu (**Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)**) sem mun innihalda breytt sniðmát verður sjálfkrafa merkt til að keyra þetta ER-snið fyrir núverandi notanda. Um leið verður hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.
3. Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður búið til sjálfkrafa.
4. Í reitnum **Athugasemd** breytirðu heiti fyrstu athugasemdar fyrir sjálfkrafa stofnaða endurskoðun á breyttu sniðmátinu.
5. Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

![Staðfesta upphaf breytingarferlis til að stofna nýtt sniðmát.](./media/BDM-Overview-EditingTemplate4.png)

Ef enginn veitandi er til staðar verður boðið upp á hann til að geta stofnað. Ef enginn virkur veitandi er til staðar verður boðið upp á hann til að velja hann fyrir virkjun.

Til að búa til veitu skal breyta heiti veitunnar í reitnum **Heiti**, uppfæra veffang nýju veitunnar í reitnum **Veffang** og velja **Í lagi** til að staðfesta.

   ![Stofna nýja veitu í BDM.](./media/bdm_create_provider.png)

Til að virkja núverandi veitanda skal velja heiti veitandans í reitnum **Skilgreiningarveitandi** og velja **Í lagi** til að stilla veitandann sem virkan.

   ![Virkja veitu í BDM.](./media/bdm_choose_provider.png)

> [!NOTE]
> Hvert BDM-sniðmát vísar í veituna sem höfund skilgreiningarinnar. Þess vegna þarf að hafa virka veitu fyrir sniðmátið.


Valkosturinn **Nýtt skjal** er alltaf í boði fyrir sniðmát með skilgreiningu ER-sniðs sem er veitt af núverandi og annarri veitu (Microsoft í þessu tilfelli) sem ekki er með neina endurskoðun. Síðan verður breytt sniðmátið geymt í nýrri skilgreiningu á ER-sniði sem er sjálfkrafa mynduð.



### <a name="start-editing-a-template"></a>Byrja á að breyta sniðmáti

1. Úr völdu sniðmáti velurðu **Breyta skjali**.
2. Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður búið til sjálfkrafa.
3. Í reitnum **Athugasemd** breytirðu heiti fyrstu athugasemdar fyrir sjálfkrafa stofnaða endurskoðun á breyttu sniðmátinu.

    ![Sniðmáti breytt á vinnusvæðasíðu viðskiptaskjalastjórnunar.](./media/BDM-Overview-EditingTemplate5.png)

4. Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

Síðan **BDM-sniðmátsritill** mun opnast. Valið sniðmát verður í boði fyrir breytingar á netinu með Microsoft 365.

![Síða sniðmátsritils viðskiptaskjalastjórnunar.](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Breyta sniðmáti í Microsoft 365

Hægt er að breyta sniðmátinu með Microsoft 365. Til dæmis, í Office á netinu skal breyta leturgerð reitakvaðninganna í sniðmáthausnum úr **Venjulegt** í **Feitletrað**. Þessar breytingar eru sjálfkrafa geymdar fyrir það breytanlega sniðmát sem er geymt í geymslu aðalsniðmátsins (sjálfgefið að það sé Azure blob-geymsla). Þetta er stillt fyrir ER ramma.

![Leturgerð breytt í feitletraða í sniðmátshausnum á síðu sniðmátsritils viðskiptaskjalastjórnunar.](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Breyta sniðmáti í Office-skjáborðsforriti

> [!NOTE]
> Þessi aðgerð er aðeins tiltæk þegar **SharePoint skjalagerð** færibreytan er rétt stillt. Nánari upplýsingar er að finna í [Skilgreina færibreytur](#SetupBdmParameters).

1. Veldu valkostinn **Opna í skjáborðsforriti** til að breyta sniðmátinu með virkni Office-skjáborðsforrits (Excel í þessu dæmi). Breytanlega sniðmátið er afritað úr varanlegri geymslu yfir í tímabundna geymslu sem er skilgreind í breytum stjórnunar viðskiptaskjala sem SharePoint-mappa.
2. Staðfestu að þú viljir opna sniðmátið úr tímabundinni skráageymslu í Excel Office-forritinu.

    ![Sniðmát opnað í Excel-skjáborðsforriti.](./media/BDM-Overview-EditingLayout3.png)

3. Breyttu sniðmátinu. Til dæmis breyta leturgerð reitakvaðninganna í sniðmáthausnum með því að uppfæra litinn úr **Svart** í **Blátt**.

    ![Breyta leturlit í sniðmátshausnum í Excel-skjáborðsforriti.](./media/BDM-Overview-EditingLayout4.png)

4. Veldu **Vista** í Excel-skjáborðsforritinu til að geyma sniðmátsbreytingarnar í tímabundinni geymslu.

    ![Vista breytingar á síðu sniðmátsritils í viðskiptaskjalastjórnun í Excel-skjáborðsforritinu.](./media/BDM-Overview-EditingLayout5.png)

5. Lokaðu Excel-skjáborðsforritinu.
6. Veldu **Samstilla geymt afrit** til að samstilla tímabundna sniðmátgeymslu við varanlega geymslu sniðmáts.

> [!NOTE]
> Afrit af breyttu sniðmátinu í tímabundnu skjalageymslunni er geymt aðeins fyrir núverandi lotu sniðmátsvinnslu. Þegar þú lýkur þessari lotu með því að loka síðunni **Ritill BDM-sniðmáts** verður þessu eintaki eytt. Ef þú lagaðir sniðmátið í tímabundnu skjalageymslu og valdir ekki **Samstilla geymt afrit** færðu skilaboð þegar þú reynir að loka síðunni **Ritstjóri BDM sniðmáts** sem spyrja hvort þú viljir geyma kynntar breytingar. Veldu **Já** ef þú vilt vista breytingarnar á sniðmátinu á varanlegri skráarstað.

### <a name="validate-a-template"></a>Villuleita sniðmát

1. Á síðunni **Ritill BDM-sniðmáts** skaltu velja **Leita að vandamálum** til að sannreyna breytt sniðmát gagnvart undirliggjandi ER-sniði. Fylgdu ráðleggingunum (ef einhverjar eru) til að samræma sniðmátið við uppbyggingu sniðsins frá grunnstillingu ER-sniðsins.
2. Veldu **Sýna snið** til að skoða núverandi uppbyggingu sniðsins frá grunnstillingu ER-sniðs sem verður að vera í takt við breytt sniðmát. 
3. Veldu **Fela snið** til að loka rúðunni.

    ![Síða BDM-sniðmátsritils.](./media/BDM-Overview-EditingTemplate6.png)

4. Lokið síðunni **BDM-sniðmátsritill**.

Uppfærða sniðmátið er sýnt á flipanum **Sniðmát**. Athugaðu að staða breytts sniðmáts er núna **Drög** og núverandi endurskoðun er ekki lengur tóm. Þetta þýðir að ferlið við að breyta þessu sniðmáti er hafið.

![Skoða uppfært sniðmát á vinnusvæðasíðu viðskiptaskjalastjórnunar.](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Prófaðu breytt sniðmát 

1. Í umsókninni, breyttu í fyrirtækið **USMF**.
2. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
3. Veldu reikninginn **FTI-00000002** og síðan **Prentstjórnun**.
4. Veldu stigið **Eining - viðskiptakröfur** \> **Skjöl** \> **Frjáls textareikningur** \> **Upprunalegt skjal** til að tilgreina umfang reikninga til vinnslu.
5. Í reitnum **Skýrslusnið** velurðu ER-sniðið **Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)** fyrir tilgreint skjalstig.

    ![Síðan Prentstýringarstilling.](./media/BDM-Overview-TestRun1.png)

6. Ýttu á **Escape** til að loka núverandi síðu.
7. Veljið **Prenta** og veljið síðan **Valið**.
8. Sæktu skjalið og opnaðu það með Excel-skjáborðsforritinu.

![Síðan Reikningar með frjálsum texta.](./media/BDM-Overview-TestRun2.png)

Breytta sniðmátið er notað til að mynda skýrslu reiknings með frjálsum texta fyrir valinn hlut. Til að greina hvernig þessi skýrsla hefur áhrif á breytingarnar sem þú gerðir í sniðmátinu geturðu keyrt þessa skýrslu í einni forritslotu beint eftir að þú breyttir sniðmátinu í annarri forritslotu.

### <a name="create-an-alternative-template-revision"></a>Búðu til aðra endurskoðun sniðmáts

1. Opnaðu síðuna **Ritill BDM-sniðmáts** og veldu sniðmátið **Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)**.
2. Á flipanum **Endurskoðanir** velurðu **Nýtt**.
3. Ef þörf er á skal í reitnum **Heiti** breyta heiti annarrar endurskoðunar og byggja hana á fyrstu endurskoðun sem er virk.
4. Ef þörf er á skal í reitnum **Athugasemd** breyta heiti fyrstu athugasemdar fyrir sjálfkrafa stofnaða endurskoðun á breyttu sniðmátinu.

    ![Búa til endurskoðanir á sniðmátinu á vinnusvæðasíðu viðskiptaskjalastjórnunar.](./media/BDM-Overview-AddRevision.png)

    Þú bjóst til nýja endurskoðun sniðmátsins sem hefur verið geymt í geymslu varanlegs sniðmáts. Nú geturðu haldið áfram að breyta sniðmátinu á annarri endurskoðuninni sem nú er valin sem virk.

5. Veldu fyrstu endurskoðunina og veldu síðan **Stilla sem virkt**. Þú getur valið aðra endurskoðun sem virka ef þú vilt einhvern tíma fara aftur í þá endurskoðun á sniðmátinu.
6. Veldu aðra endurskoðunina og smelltu svo á **Eyða**.
7. Veldu **Í lagi** til að staðfesta að þú viljir eyða valinni endurskoðun. Þú getur eytt öllum óvirkum endurskoðunum þegar ekki er þörf á þeim lengur.

### <a name="delete-a-modified-template"></a>Eyða breyttu sniðmáti

1. Á síðunni **Ritill BDM-sniðmáts** velurðu flipann **Sniðmát**.
2. Veljið **Eyða**.
3. Ef þú velur **Í lagi** til að staðfesta eyðingu verður ER-sniðinu **Afrit af skýrslu viðskiptamanna með frjálsum texta (GER)** með breyttu sniðmáti eytt. Veldu **Hætta við** til að kanna aðra valkosti.

### <a name="revoke-changes-of-template"></a>Afturkalla breytingar á sniðmáti

Þegar þú breytir sniðmátinu úr ER-sniði sem er í eigu núverandi virks veitanda færðu þann valkost að afturkalla breytingar sem gerðar voru á sniðmátinu.

![Hafna breytingum á sniðmátinu á vinnusvæðasíðu viðskiptaskjalastjórnunar.](./media/BDM-Overview-RevokeChanges.png)

1. Á síðunni **Ritill BDM-sniðmáts** velurðu flipann **Sniðmát**.
2. Veldu **Afturkalla**.
3. Ef þú velur **Í lagi** til að afturkalla breytingarnar sem gerðar voru á sniðmátinu verður breyttu sniðmáti skipt út fyrir upprunalega sniðmátið og allar breytingar fjarlægðar. Þegar þú afturkallar breytingar á sniðmátinu muntu geta eytt því. Veldu **Hætta við** til að kanna aðra valkosti.

### <a name="publish-a-modified-template"></a>Gefa út breytt sniðmát

1. Á síðunni **Ritill BDM-sniðmáts**, á flipanum **Sniðmát**, velurðu **Gefa út**.
2. Ef þú velur **Í lagi** til að staðfesta útgáfu verða drög að útgáfu á afleidda ER-sniðinu **Afrit af skýrslu viðskiptamanna með frjálsum texta (GER)** sem inniheldur breytt sniðmát merkt sem lokið. Breytta sniðmátið verður tiltækt fyrir aðra notendur. Loknu útgáfurnar af þessu ER-sniði munu aðeins halda síðustu virku endurskoðun sniðmátsins. Öðrum endurskoðunum verður eytt. Veldu **Hætta við** til að kanna aðra valkosti.

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Ég valdi Breyta skjali, en í stað þess að fara á síðu BDM-sniðmátsritils í Finance var mér vísað á vefsíðu Microsoft 365.

Þetta vandamál er þekkt vandamál sem hefur með framsendingu Microsoft 365 að gera. Það kemur upp þegar þú skráir þig inn í Microsoft 365 í fyrsta skipti. Til að vinna í kringum þetta vandamál skal velja **Til baka** í vafranum til að fara aftur á fyrri síðu.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>Ég skil hvernig á að breyta sniðmáti með Microsoft 365 í fyrstu hugbúnaðarlotunni og hvernig nota á sniðmátið í seinni forritalotunni sem leiðréttir sniðmátið til að sjá hvernig breytingarnar mínar hafa áhrif á myndað viðskiptaskjal. Er hægt að nota Office-skjáborðsforritið á sama hátt?

Já, það er hægt. Veldu í fyrstu forritslotunni **Opna í skjáborðsforriti**. Sniðmátið þitt verður geymt í tímabundinni skráageymslu og opnað í Office-skjáborðsforritinu. Næst skaltu ljúka eftirfarandi skrefum til að forskoða sniðmátsbreytingarnar í mynduðu viðskiptaskjali:

1. Gerðu breytingar á sniðmátinu með því að nota Office-skjáborðsforritið.
2. Veldu **Vista** í Office-skjáborðsforritinu.
3. Á síðunni **Ritill BDM-sniðmáts** í fyrstu forritslotunni velurðu **Samstilla geymt afrit**.
4. Framkvæmdu þetta sniðmát ER-sniðs í annarri umsóknarlotunni.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Þegar ég vel Opna í skjáborðsforritinu koma upp eftirfarandi villuboð: „Gildið má ekki vera núll. Heiti færibreytu: externalId.“ Hvernig leysi ég vandamálið?

Líklegast skráðir þú þig inn í núverandi tilvik forritsins í Azure AD-léni sem er frábrugðið því Azure AD-léni sem var notað til að dreifa þessu tilviki Finance and Operations. Vegna þess að SharePoint-þjónustan, sem er notuð til að geyma sniðmát til að gera þau aðgengileg fyrir breytingu með Office-skjáborðsforritum, tilheyrir sama léni, höfum við engar heimildir til að fá aðgang að SharePoint-þjónustunni. Til að leysa þetta mál skaltu skrá þig inn í núverandi tilvik af með því að nota skilríki notanda með réttu Azure AD-léni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md)

[Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði (nóvember 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði](tasks/er-design-configuration-word-2016-11.md)

[Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md)

[Skilgreina rafræna skýrslugerð til að draga gögn inn í Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>Listi yfir skilgreiningar rafrænnar skýrslugerðar sem hafa verið gefnar út í Finance til að styðja skilgreinanleg viðskiptaskjöl

Sífellt er verið að uppfæra [Listann](general-electronic-reporting.md#list-of-configurations) yfir skilgreiningar rafrænnar skýrslugerðar fyrir Finance. Opnið [Altæka geymsla](er-download-configurations-global-repo.md) til að fara yfir lista yfir skilgreiningar rafrænnar skýrslugerðar sem eru studdar. Hægt er að [sía](../../../finance/localizations/enhanced-filtering-global-repo.md) altæka geymslu til að fara yfir lista yfir skilgreiningar rafrænnar skýrslugerðar sem eru notaðar til að styðja skilgreinanleg viðskiptaskjöl.

![Efni altækrar geymslu síað á síðu skilgreiningageymslu.](./media/bdm-overview-filterglobalrepo.gif)

Eftirfarandi tafla sýnir lista yfir skilgreiningar rafrænnar skýrslugerðar sem styðja skilgreinanleg viðskiptaskjöl og hafa verið gefnar út í Finance fram að desember 2020.

| Skilgreining gagnalíkans    | Sníða skilgreiningar                           |
|-----------------------------|-------------------------------------------------|
| Líkan farmbréfs        | Farmbréf (Excel)                          |
|                             | Farmbréf (Word)                           |
| Líkan upprunavottorðs | Upprunavottorð (Excel)                   |
|                             | Upprunavottorð (Word)                    |
| Reikningslíkan               | Debet- og kreditnóta viðskiptavinar (Excel)          |
|                             | Debet- og kreditnóta viðskiptavinar (Word)           |
|                             | Reikningur með frjálsum texta (Excel)                       |
|                             | Reikningur með frjálsum texta (Excel) (BH)                  |
|                             | Reikningur með frjálsum texta (FR) (Excel)                  |
|                             | Reikningur með frjálsum texta (LT) (Excel)                  |
|                             | Reikningur með frjálsum texta (LV) (Excel)                  |
|                             | Reikningur með frjálsum texta (PL) (Excel)                  |
|                             | Reikningur með frjálsum texta (CZ) (Excel)                  |
|                             | Reikningur með frjálsum texta (EE) (Excel)                  |
|                             | Reikningur með frjálsum texta (HU) (Excel)                  |
|                             | Reikningur með frjálsum texta (TH) (Excel)                  |
|                             | Reikningur með frjálsum texta (Word)                        |
|                             | Atriði verksamningslínu (Excel)             |
|                             | Atriði verksamningslínu (CZ) (Excel)        |
|                             | Atriði verksamningslínu (Excel) (BH)        |
|                             | Atriði verksamningslínu (HU) (Excel)        |
|                             | Atriði verksamningslínu (LT) (Excel)        |
|                             | Atriði verksamningslínu (PL) (Excel)        |
|                             | Atriði verksamningslínu (Word)              |
|                             | Varðveislulosun á verki viðskiptavinar (Excel)      |
|                             | Varðveislulosun á verki viðskiptavinar (CZ) (Excel) |
|                             | Varðveislulosun á verki viðskiptavinar (HU) (Excel) |
|                             | Varðveislulosun á verki viðskiptavinar (LT) (Excel) |
|                             | Varðveislulosun á verki viðskiptavinar (PL) (Excel) |
|                             | Varðveislulosun á verki viðskiptavinar (TH) (Excel) |
|                             | Varðveislulosun á verki viðskiptavinar (Word)       |
|                             | Verkreikningur (Excel)                         |
|                             | Verkreikningur (Word)                          |
|                             | Verkreikningur (AE) (Excel)                    |
|                             | Verkreikningur (CZ) (Excel)                    |
|                             | Verkreikningur (Excel) (BH)                    |
|                             | Verkreikningur (HU) (Excel)                    |
|                             | Verkreikningur (JP) (Excel)                    |
|                             | Verkreikningur (LT) (Excel)                    |
|                             | Verkreikningur (PL) (Excel)                    |
|                             | Verkreikningur (TH) (Excel)                    |
|                             | Ítarlegur verkreikningur (MY) (Excel)               |
|                             | Einfaldur verkreikningur (MY) (Excel)             |
|                             | Stjórna verkreikningi (Excel)                  |
|                             | Stjórna verkreikningi (CZ) (Excel)             |
|                             | Stjórna verkreikningi (Excel) (BH)             |
|                             | Stjórna verkreikningi (HU) (Excel)             |
|                             | Stjórna verkreikningi (JP) (Excel)             |
|                             | Stjórna verkreikningi (LT) (Excel)             |
|                             | Stjórna verkreikningi (PL) (Excel)             |
|                             | Stjórna verkreikningi (Word)                   |
|                             | Reikningur fyrir innkaup og fyrirframgreiðslu (Excel)                |
|                             | Reikningur fyrir innkaup og fyrirframgreiðslu (Word)                 |
|                             | Reikningur fyrir sölu og fyrirframgreiðslu (Excel)                   |
|                             | Reikningur fyrir sölu og fyrirframgreiðslu (Word)                    |
|                             | Reikningur fyrir sölu og fyrirframgreiðslu (PL) (Excel)              |
|                             | Sölureikningur (Excel)                           |
|                             | Sölureikningur (Excel) (BH)                      |
|                             | Sölureikningur (Excel) (CZ)                      |
|                             | Sölureikningur (Excel) (EE)                      |
|                             | Sölureikningur (Excel) (FR)                      |
|                             | Sölureikningur (Excel) (HU)                      |
|                             | Sölureikningur (Excel) (IN)                      |
|                             | Sölureikningur (Excel) (LT)                      |
|                             | Sölureikningur (Excel) (LV)                      |
|                             | Sölureikningur (Excel) (PL)                      |
|                             | Sölureikningur (Excel) (TH)                      |
|                             | Sölureikningur (Word)                            |
|                             | TMS-viðskiptareikningur (Excel)                  |
|                             | TMS-viðskiptareikningur (Word)                   |
|                             | Reikningsskjals lánardrottins (Excel)                 |
|                             | Reikningsskjal lánardrottins (CZ) (Excel)            |
|                             | Reikningsskjal lánardrottins (HU) (Excel)            |
|                             | Reikningsskjal lánardrottins (IN) (Excel)            |
|                             | Reikningsskjal lánardrottins (LT) (Excel)            |
|                             | Reikningsskjal lánardrottins (LV) (Excel)            |
|                             | Reikningsskjal lánardrottins (MY) (Excel)            |
|                             | Reikningsskjal lánardrottins (Word)                  |
| Pöntunarlíkan                 | Staðfesting samnings (Excel)                  |
|                             | Staðfesting samnings (Word)                   |
|                             | Staðfesting á innkaupasamningi (Excel)         |
|                             | Staðfesting á innkaupasamningi (Word)          |
|                             | Innkaupapöntun (Excel)                          |
|                             | Innkaupapöntun (CZ) (Excel)                     |
|                             | Fyrirspurn um innkaupapöntun (CZ) (Excel)             |
|                             | Innkaupapöntun (HU) (Excel)                     |
|                             | Fyrirspurn um innkaupapöntun (HU) (Excel)             |
|                             | Númer innkaupapöntunar (Word)                           |
|                             | Fyrirspurn um innkaupapöntun (Excel)                  |
|                             | Fyrirspurn um innkaupapöntun (Word)                   |
|                             | Staðfesting sölupöntunar (Excel)                |
|                             | Staðfesting sölupöntunar (CZ) (Excel)           |
|                             | Staðfesting sölupöntunar (HU) (Excel)           |
|                             | Staðfesting sölupöntunar (Word)                 |
| Líkan pökkunarlista          | Innihald gáms (Excel)                      |
|                             | Innihald gáms (Word)                       |
|                             | Farmlisti (Excel)                               |
|                             | Farmlisti (Word)                                |
|                             | Tiltektarlisti (Excel)                            |
|                             | Tiltektarlisti (CZ) (Excel)                       |
|                             | Tiltektarlisti (Word)                             |
|                             | Tiltektarlisti framleiðslu (Excel)                    |
|                             | Tiltektarlisti framleiðslu (Word)                     |
|                             | Sendingartiltektarlisti fyrir farm (Excel)             |
|                             | Sendingartiltektarlisti fyrir farm (Word)              |
|                             | Sendingartiltektarlisti fyrir sendingu (Excel)         |
|                             | Sendingartiltektarlisti fyrir sendingu (Word)          |
|                             | Sendingartiltektarlisti fyrir bylgju (Excel)             |
|                             | Sendingartiltektarlisti fyrir bylgju (Word)              |
| Greiðslulíkan               | Greiðslutilkynning viðskiptavinar (Excel)                 |
|                             | Greiðslutilkynning viðskiptavinar (Word)                  |
|                             | Greiðslutilkynning lánardrottins (Excel)                   |
|                             | Greiðslutilkynning lánardrottins (Word)                    |
| Tilboðslíkan             | Verktilboð (Excel)                       |
|                             | Kenni verktilboðs (Word)                        |
|                             | Beiðni um tilboð (Excel)                   |
|                             | Beiðni um tilboð (samþykkja) (Excel)          |
|                             | Beiðni um tilboð - (Samþykkja) (Word)           |
|                             | Beiðni um tilboð - (Hafna) (Excel)          |
|                             | Beiðni um tilboð - (Hafna) (Word)           |
|                             | Beiðni um tilboð - (Skil) (Excel)          |
|                             | Beiðni um tilboð (Skil) (Word)           |
|                             | Beiðni um tilboð (Word)                    |
|                             | Sölutilboð (Excel)                         |
|                             | Sölutilboð (CZ) (Excel)                    |
|                             | Sölutilboð (HU) (Excel)                    |
|                             | Sölutilboð (Word)                          |
|                             | Staðfesting sölutilboðs (Excel)            |
|                             | Staðfesting sölutilboðs (Word)             |
| Afstemmingarlíkan        | Reikningsyfirlit viðskiptavinar, ext (Excel)             |
|                             | Reikningsyfirlit viðskiptavinar, ext (CN) (Excel)        |
|                             | Reikningsyfirlit viðskiptavinar, ext (Word)              |
|                             | Reikningsyfirlit viðskiptavinar, Frakkland (Excel)          |
| Áminningarlíkan              | Innheimtubréfsnóta (Excel)                  |
|                             | Innheimtubréfsnóta (CN) (Excel)             |
|                             | Innheimtubréfsnóta (Word)                   |
|                             | Vaxtanóta viðskiptavinar (Excel)                  |
|                             | Vaxtanóta viðskiptavinar (Word)                   |
| Líkan farmskráar               | Farmtilboð (Excel)                             |
|                             | Farmtilboð (Word)                              |
|                             | Fylgiseðill innkaupapöntunar (Excel)             |
|                             | Fylgiseðill innkaupapöntunar (CZ) (Excel)        |
|                             | Fylgiseðill innkaupapöntunar (Word)              |
|                             | Leið (Excel)                                   |
|                             | Leið (Word)                                    |
|                             | Fylgiseðill sölupöntunar (Excel)                |
|                             | Fylgiseðill sölupöntunar (CZ) (Excel)           |
|                             | Fylgiseðill sölupöntunar (LT) (Excel)           |
|                             | Fylgiseðill sölupöntunar (PL) (Excel)           |
|                             | Sölupöntun - Fylgiseðill (Word)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
