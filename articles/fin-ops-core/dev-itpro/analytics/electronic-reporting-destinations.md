---
title: Áfangastaðir fyrir rafræna skýrslugerð
description: Í þessu efnisatriði er að finna upplýsingar um stjórnun á áfangastöðum rafrænnar skýrslugerðar, gerðir studdra áfangastaða og öryggissjónarmið.
author: nselin
ms.date: 05/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 088f1b13e20602345dbec5179c343e27be9cec44
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085501"
---
# <a name="electronic-reporting-er-destinations"></a>Áfangastaðir fyrir rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Hægt er að skilgreina áfangastað inn fyrir hverja skilgreiningarsnið Rafrænnar skýrslugerðar (ER) og íhlut úttaks þess (möppu eða í skrá). Notendur sem eru veittar viðeigandi aðgangsheimildir einnig er hægt að breyta stillingar fyrir áfangastað á keyrslutíma. Þetta efni útskýrir áfangastaðastjórnun rafrænnar skýrslugerðar, gerðir áfangastaða sem eru studdar, og öryggisatriði.

ER-skilgreiningar sniðs innihalda yfirleitt minnst einn frálagsíhlut: skrá. Skilgreiningar innihalda yfirleitt margar frálagsíhluti skráa af mismunandi gerðum (t.d. XML, TXT, XLSX, DOCX eða PDF) sem eru flokkaðar í annað hvort í einni möppu eða margar möppur. Stjórnun áfangastaðar Rafrænnar skýrslugerðar gerir kleift að forstilla hvað gerist þegar hver íhlutur er keyrður. Að sjálfgefnu þegar afbrigði er keyrð, sér notandi svarglugga sem er hægt að nota til að vista eða opna skrána. Sama hegðun kemur einnig upp þegar þú flytur inn skilgreiningu rafrænnar skýrslugerðar og skilgreinir ekki tilteknu áfangastaði fyrir hana. Eftir á ákvörðunarstað hefur verið stofnuð fyrir aðal frálagsíhlut, hnekkir sá ákvörðunarstað sjálfgefinni hegðun og möppu eða skráin er send samkvæmt stillingum áfangastaðar.

## <a name="availability-and-general-prerequisites"></a>Framboð og almenn skilyrði

Virkni fyrir ER-áfangastaði er ekki tiltæk í Microsoft Dynamics AX útgáfu 7.0 (febrúar 2016). Þess vegna verður þú að setja upp Microsoft Dynamics 365 for Operations útgáfu 1611 (nóvember 2016) eða síðar til að nota eftirfarandi áfangastaðategundir:

- [Netfang](er-destination-type-email.md)
- [Safnvista](er-destination-type-archive.md)
- [Skrá](er-destination-type-file.md)
- [Skjár](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Einnig er hægt að setja upp einn af eftirfarandi skilyrðum. Hins vegar þarftu að athuga að þessir valkostir veita meira takmarkað rafræna skýrslugerð viðtökustaður upplifun.

- Microsoft Dynamics AX-forrit, útgáfa 7.0.1 (maí 2016)
- [Leiðbeiningar um bráðabót skýrslugjafar ákvörðunarstaðar](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Það er líka a [Prenta](er-destination-type-print.md) tegund ákvörðunarstaðar. Til að nota það verður þú að setja upp Microsoft Dynamics 365 Finance útgáfu 10.0.9 (apríl 2020).

## <a name="overview"></a>Yfirlit

Hægt er að setja upp áfangastaði aðeins fyrir skilgreiningar rafrænnar skýrslugerðar sem hafa verið [fluttar inn](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) í gildandi tilvik Finance og fyrir sniðin sem eru tiltæk á síðunni **Skilgreiningar rafrænnar skýrslugerðar**. Virkni ER-stjórnunar áfangastaða er tiltæk á **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.

### <a name="default-behavior"></a>Sjálfgefin hegðun

Sjálfgefin hegðun fyrir skilgreiningu sniðs rafrænnar skýrslugerðar veltur á keyrslugerð sem er tilgreind þegar það hefst.

Í svarglugganum **Intrastat-skýrsla** á flipanum **Keyra í bakgrunni**, ef valkosturinn **Runuvinnsla** er stilltur á **Nei** er snið rafrænnar skýrslugerðar keyrt strax í gagnvirkri stillingu. Þegar þessari keyrslu er lokið er hægt að sækja tilbúið skjal á útleið.

Ef valkosturinn **Runuvinnsla** er stilltur á **Já** er snið rafrænnar skýrslugerðar keyrt í stillingunni [runa](../sysadmin/batch-processing-overview.md). Viðeigandi runuvinnsla er stofnuð á grundvelli færibreytna sem tilgreindar eru í **Keyra í bakgrunni** flipa í flipanum í svarglugganum **Færibreytur rafrænnar skýrslugerðar** .

> [!NOTE]
> Starfslýsing lætur vita um keyrslu á vörpun með sniði rafrænnar skýrslugerðar. Hún inniheldur einnig heiti rafræns skýrslugerðarhluts sem er keyrður.

[![Keyrir snið rafrænnar skýrslugerðar](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Hægt er að fá upplýsingar um þetta starf á nokkrum stöðum:

- Farið á **Almennt** \> **Fyrirspurnir** \> **Runuvinnslur** \> **Runuvinnslur mínar** til að skoða stöðu áætlaðrar vinnslu.
- Opnaðu **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Rafræn skýrslugerðarvinnsla** til að skoða stöðu áætlaðrar vinnslu og niðurstöður lokinna verka. Þegar vinnslunni er lokið skal velja **Sýna skrár** á síðunni **Rafræn skýrslugerðarvinnsla** til að fá skjal á útleið.

    > [!NOTE]
    > Þetta skjal er vistað sem viðhengi núverandi vinnslufærslu og er stjórnað af ramma [Skjalastjórnun](../../fin-ops/organization-administration/configure-document-management.md). [Skjalagerðin](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) sem er notuð til að vista ER gervinga af þessari gerð eru stilltir í [ER færibreytum](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- Á síðunni **Rafræn skýrslugerðarvinnsla** skal velja **Sýna skrár** til að skoða lista yfir hugsanlegar villur og viðvaranir sem komu fram við keyrslu.

    [![Skoða starfalista rafrænnar skýrslugerðar](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Notandaskilgreind hegðun

Á síðunni **Viðtökustaður rafrænnar skýrslugerðar** er hægt að hnekkja sjálfgefinni hegðun fyrir stillingar. Innfluttar skilgreiningar eru ekki sýnd á þessari síðu fyrr en þú velur **Nýtt** og síðan, í reitnum **Tilvísun** skal velja skilgreiningu til að stofna stillingar fyrir áfangastað fyrir.

[![Velja skilgreiningu í svæðinu Tilvísun](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Eftir að þú hefur búið til tilvísun geturðu búið til skráarmiðstöð fyrir sérhvert heiti úttaksþáttar **Möppu** eða **Skráar** af tilvísuðu ER-sniði.

[![Stofnun viðtöðustaðar skráar](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Því næst, í svarglugganum **Stillingar fyrir áfangastað** geturðu virkjað og afvirkjað staka áfangastaði fyrir áfangastað skráar. **Stillingar** hnappinn er notuð til að stjórna áfangastaði fyrir valinn áfangastað skrár. Í **stillingar fyrir Áfangastað** svarglugganum er hægt að stjórna hvern ákvörðunarstað sérstaklega með því að stilla **Virkt** valkost fyrir hana.

Í útgáfum af Finance **á undan útgáfu 10.0.9** er hægt að stofna **einn viðtökustað skráar** fyrir hvern úttaksþátt á sama sniði, eins og möppu eða skrá sem er valin í reitnum **Skráarheiti**. Hins vegar, í **útgáfa 10.0.9 og nýrri** er hægt að stofna **áfangastaði fyrir margar skrár** fyrir hvern úttaksþátt með sama sniði.

Til dæmis er hægt að nota þessa getu til að stilla skrá áfangastaða fyrir skráhluta sem er notaður til að búa til skjal á útleið á Excel sniði. Einn ákvörðunarstaður ([Skjalasafn](er-destination-type-archive.md)) er hægt að stilla til að geyma upprunalegu Excel skrána í skjalasafni ER-starfa og á öðrum ákvörðunarstað ([Netfang](er-destination-type-email.md)) er hægt að stilla til að samtímis [umbreyta](#OutputConversionToPDF) Excel-skjalið á PDF snið og senda PDF-skjalið með tölvupósti.

[![Stilla marga áfangastaði fyrir staka sniðeiningu](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Þegar snið rafrænnar skýrslugerðar er keyrt verða allir áfangastaðir sem voru skilgreindir fyrir íhluti sniðsins alltaf keyrðir. Að auki, í Finance **útgáfu 10.0.17 og nýrri**, hefur virkni áfangastaða rafrænnar skýrslugerðar verið bætt og gerir notanda nú kleift að skilgreina mismunandi safn staðsetninga fyrir eitt snið rafrænnar skýrslugerðar. Þessi skilgreining merkir hvert safn sem skilgreint fyrir tiltekna aðgerð notanda. API rafrænnar skýrslugerðar hefur verið [stækkað](er-apis-app10-0-17.md) þannig að hægt sé að bjóða upp á aðgerð sem notandi framkvæmir með því að keyra snið rafrænnar skýrslugerðar. Aðgerðarkóðinn sem er veittur er sendur til áfangastaða rafrænnar skýrslugerðar. Hægt er að keyra mismunandi áfangastaði fyrir snið rafrænnar skýrslugerðar, sem fer eftir aðgerðarkóðanum sem gefinn er upp. Frekari upplýsingar er að finna í [Skilgreina áfangastaði rafrænnar skýrslugerðar sem eru háðir aðgerð](er-action-dependent-destinations.md).

## <a name="destination-types"></a>Gerðir viðtökustaða

Eftirfarandi áfangastaðir eru nú studdir fyrir ER-snið. Þú getur virkjað eða óvirkjað allar gerðir á sama tíma. Á þennan hátt er annað hvort hægt að gera ekkert eða senda íhlutinn á allar skilgreinda áfangastaði.

- [Netfang](er-destination-type-email.md)
- [Safnvista](er-destination-type-archive.md)
- [Skrá](er-destination-type-file.md)
- [Skjár](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Prentun](er-destination-type-print.md)

## <a name="applicability"></a>Gildissvið

Hægt er að setja upp áfangastaði aðeins fyrir skilgreiningar rafrænnar skýrslugerðar sem hafa verið fluttar inn, og fyrir sniðin sem eru tiltækir í **skilgreiningar rafrænnar skýrslugerðar** síðu.

> [!NOTE]
> Stilltir áfangastaðir eru fyrirtækjasértækir. Ef þú ætlar að nota ER-snið í mismunandi fyrirtækjum á núverandi tilviki Finance verður þú að stilla áfangastaði fyrir það ER-snið fyrir hvert þessara fyrirtækja.

Þegar þú stillir skrá áfangastaða fyrir valið snið stillirðu þær fyrir allt sniðið.

[![Skilgreiningartengill](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Á sama tíma gætir þú átt margar [útgáfur](general-electronic-reporting.md#component-versioning) af því sniði sem hefur verið flutt inn í núverandi tilviki Finance. Þú getur skoðað þau ef þú velur tengilinn **Stillingar** sem er í boði þegar þú velur reitinn **Tilvísun**.

[![Útgáfur grunnstillingarinnar](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Sjálfgefið er að stilla áfangastaði er aðeins beitt þegar þú keyrir ER sniðútgáfu sem hefur annaðhvort stöðuna **Lokið** eða **Deilt**. Hins vegar verður þú stundum að nota stillta áfangastaði þegar drög að útgáfu ER sniðs er keyrt. Til dæmis, þú breytir drög að útgáfu af sniðinu þínu, og þú vilt nota stillta áfangastaði til að prófa hvernig mynda framleiðsla verður afhent. Fylgdu þessum skrefum til að beita ákvörðunarstöðum fyrir ER snið þegar drög að útgáfu eru keyrð.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Stilltu valkostinn **Nota áfangastaði fyrir drög** á **Já**.

[![Valkosturinn Nota áfangastaði fyrir drög](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Til að nota drög útgáfu af ER sniði verður þú að merkja ER sniðið í samræmi við það.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Stillið valkostinn **Keyra stillingar** á **Já**.

[![Keyra stillingarvalkost](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Eftir að þú hefur lokið þessari uppsetningu verður valkosturinn **Keyra drög** í boði fyrir ER-snið sem þú breytir. Stilltu þennan valkost á **Já** til að byrja að nota drög að sniðinu þegar sniðið er keyrt.

[![Valkosturinn Keyra drög](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Villumeðhöndlun ákvörðunarstaðar

Venjulega er ER snið keyrt innan gildissviðs ákveðins viðskiptaferlis. Hins vegar verður afhending á útgefnu skjali sem myndast við framkvæmd ER sniðs stundum að teljast hluti af því viðskiptaferli. Í þessu tilfelli, ef afhending á mynduðu útgefnu skjali til uppsetts ákvörðunarstaðar er ekki árangursrík, verður að hætta við framkvæmd viðskiptaferlisins. Til að stilla viðeigandi ER áfangastað, veldu valkostinn **Hætta að vinna við villu**.

Til dæmis stillirðu greiðsluvinnslu lánardrottins þannig að **ISO20022 lánaflutningur** ER snið er keyrt til að búa til greiðsluskrá og viðbótargögn (til dæmis fylgibréf og eftirlitsskýrsla). Ef aðeins ætti að líta á greiðslu sem afgreidda með góðum árangri ef fylgibréfið er afhent með tölvupósti, verður þú að velja gátreitinn **Hætta að vinna við bilun** fyrir hlutann **CoveringLetter** í viðeigandi skráarstað, eins og sýnt er á eftirfarandi mynd. Í þessu tilfelli verður staða greiðslunnar sem er valin til vinnslu breytt úr **Ekkert** í **Sent** aðeins þegar fylgibréfið sem er búið til er samþykkt til afhendingar hjá tölvupóstveitunni sem er stilltur í Finance-tilvikinu.

[![Stilla ferlismeðhöndlun fyrir bilun viðtökustaðar skráa](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Ef þú hreinsar gátreitinn **Hætta að vinna við bilun** fyrir hlutann **CoveringLetter** í áfangastaðnum, mun greiðsla teljast hafa tekist jafnvel þó að upplýsingabréf hafi ekki borist í tölvupósti. Stöðu greiðslunnar verður breytt úr **Ekkert** í **Sent** jafnvel þó ekki sé hægt að senda fylgibréf vegna þess að til dæmis vantar póstfang viðtakanda eða sendanda eða rangt.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Útfærsla í PDF

Hægt er að nota valkost PDF-umbreytingar til að breyta úttaki í Microsoft Office (Excel eða Word) sniði yfir á PDF-snið.

### <a name="make-pdf-conversion-available"></a>Gerðu PDF umbreytingu aðgengileg

Til að gera PDF umbreytingarvalkostinn tiltækan í núverandi tilviki Finance, opnaðu vinnusvæðið **Stjórnun eiginleika** og kveiktu á eiginleikanum **Umbreyta skjölum á útleið í rafrænni skýrslugerð úr Microsoft Office-sniði á PDF**.

[![Kveikt á PDF umbreytingu skjala á útleið í Stjórnun eiginleika](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Gildissvið

Aðeins er hægt að kveikja á valkosti PDF-umbreytingar fyrir skráarhluta sem eru notaðir til að mynda úttak á Office-sniði (Excel eða Word) (**Excel-skrá**). Þegar kveikt er á þessum valkosti er úttak sem er myndað á Office sniði sjálfkrafa breytt í PDF snið. Í útgáfum Finance **á undan útgáfu 10.0.18** er aðeins hægt að kveikja á þessum valkosti fyrir þætti af gerðinni **Excel\\skrá** sem eru notaðir til að mynda úttak á [Excel-sniði](er-fillable-excel.md) eða [Word-sniði](er-design-configuration-word.md). Í **útgáfu 10.0.18 og nýrri** er hins vegar einnig hægt að kveikja á þessum valkosti fyrir þætti af gerðinni **Algeng\\skrá**.

> [!NOTE]
> Athugið villuboðin sem koma upp þegar kveikt er á valkosti PDF-breytingar fyrir rafræna skýrslugerðarþætti af gerðinni **Algeng\\skrá**. Þessi skilaboð gefa til kynna að ekki sé hægt að tryggja, á hönnunartíma, að valinn skráarþáttur muni sýna efnið á PDF-sniði eða efni sem umbreytt er yfir í PDF á keyrslutíma. Því ætti aðeins að kveikja á valkostinum ef öruggt er að valinn skráarþáttur hafi verið skilgreindur til að sýna efni á PDF-sniði eða efni sem umbreytt er yfir í PDF á keyrslutíma.
> 
> Ef kveikt er á valkosti PDF-umbreytingar fyrir þátt af gerðinni **Excel\\skrá**, ef sá þáttur sýnir efni á sniði öðru en PDF, og ef ekki er hægt að umbreyta sýnt efni yfir á PDF-snið, mun undantekning eiga sér stað á keyrslutíma. Skilaboðin sem koma upp segja að ekki sé hægt að umbreyta myndað efni yfir á PDF-snið.

### <a name="limitations"></a>Takmarkanir

Valkostur PDF-umbreytingar er aðeins í boði fyrir uppsetningar í skýi.

PDF-skjalið sem verður til takmarkast við að hámarki 300 blaðsíður.

Í Finance, **útgáfu 10.0.9**, er aðeins langsnið á síðum stutt í PDF-skjalinu sem er búið til úr Excel-úttaki. Í Finance, **útgáfu 10.0.10 (maí 2020) og nýrri**, er hægt að [tilgreina hvernig blaðsíðan á að snúa](#SelectPdfPageOrientation) fyrir PDF-skjal sem er búið til úr Excel-úttaki á meðan staðsetning rafrænnar skýrslugerðar er skilgreind.

Aðeins algengar leturgerðir Windows-stýrikerfisins eru notaðar til að umbreyta úttaki sem inniheldur engar innfelldar leturgerðir.

### <a name="use-the-pdf-conversion-option"></a>Notaðu PDF-umbreytingarvalkostinn

Til að kveikja á PDF-ummyndun fyrir skráarstað, veldu gátreitinn **Umbreyta í PDF**.

[![Kveikt á PDF-ummyndun fyrir skráarstað](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Veldu síðu stefnu fyrir PDF umbreytingu</a>

Ef skilgreining rafrænnar skýrslugerðar er búin til á Excel-sniði og ætlunin er að breyta því í PDF-skjal, er hægt að tilgreina hvernig síðan á að snúa í PDF-skjalinu. Þegar þú velur gátreitinn **Umbreyta í PDF** til að kveikja á PDF umbreytingu fyrir skráarstað sem framleiðir úttaksskrá á Excel-sniði verður reiturinn **Síðustefna** fáanlegur á flýtiflipanum **PDF-umbreytingarstillingar**. Í reitnum **Síðustefna** velurðu valda stefnu.

[![Val á síðustefnu fyrir PDF-umbreytingu](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

> [!NOTE]
> Til að hafa möguleikann á því að velja hvernig PDF-síða á að snúa þarf að setja upp Finance-útgáfu 10.0.10 eða nýrri.
>
> Valin síðustefna er notuð á allar ER stillingar sem eru búnar til á Excel sniði og síðan breytt í PDF snið.
>
> Ef skilgreining rafrænnar skýrslugerðar á Word-sniði er breytt í PDF-snið, verður snúningur PDF-skjalsins tekinn frá Word-skjalinu.

## <a name="output-unfolding"></a>Framsetning úttaks

Þegar viðtökustaður er skilgreindur fyrir hlutinn **Mappa** í rafræna skýrslugerðarsniðinu, er hægt að tilgreina hvernig úttak hlutarins er skilað á skilgreindan viðtökustað.

### <a name="make-output-unfolding-available"></a>Gera framsetningu úttaks aðgengilegan

Til að gera valkost á framsetningu úttaks aðgengilegan í núverandi tilviki af Finance skal opna vinnusvæðið **Eiginleikastjórnun** og kveikja á eiginleikanum **Leyfa skilgreiningu áfangastaða rafrænnar skýrslugerðar til að senda innihald möppu sem aðskildar skrár**.

### <a name="applicability"></a>Gildissvið

Aðeins er hægt að skilgreina framsetningu úttaks fyrir sniðshluta af gerðinni **Mappa**. Þegar hafist er handa við að skilgreina **Möppuhlutann** verður flýtiflipinn **Almennt** í boði á síðunni **Viðtökustaður rafrænnar skýrslugerðar**. 

### <a name="use-the-output-unfolding-option"></a>Nota framsetningarvalkost úttaks

Í flýtiflipanum **Almennt**, í reitnum **Senda möppu sem**, skal velja eitt af eftirfarandi gildum:

- **ZIP-safnskrá** – Afhenda myndaða skrá sem zip-skrá.
- **Aðskildar skrár** – Afhenda allar skrár myndaðrar zip-skráar sem einstaka skrá.

    > [!NOTE]
    > Þegar **Aðskildar skrár** er valið er myndað úttak safnað í minni á þjöppuðu formi. Þar af leiðandi gildir [hámarksstærð skráar](er-compress-outbound-files.md) fyrir þjappað úttak þegar raunveruleg skráarstærð fer yfir þessi mörk. Mælt er með því að velja þetta gildi þegar búist er við því að stærð myndaðs úttaks verði of stórt.

[![Skilgreina viðtökustað fyrir hlut möppusniðs](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>Takmarkanir

Ef reiturinn **Senda möppu sem** er stilltur á **Aðskildar skrár** fyrir **Möppuhluta** sem inniheldur annan faldaðan **Möppuhluta** er stilllingin ekki notuð endurkvæmt á faldaða **Möppuhluta**.

## <a name="security-considerations"></a>Öryggisatriði

Tvær gerðir af skyldum og réttindum eru notaðar fyrir áfangastaði rafrænnar skýrslugerðar. Ein gerð stjórnar heildarmöguleika notanda á að viðhalda almennum áfangastaði sem eru skilgreind fyrir lögaðila (það er, hún stjórnar aðgangi að **áfangastöðum rafrænnar skýrslugerðar** síðu). Önnur gerð stjórnar möguleika notanda forrits til að hnekkja, á keyrslutíma, stillingarnar áfangastaðar sem eru skilgreind af forritara rafrænnar skýrslugerðar eða hagnýtur ráðgjafi rafrænnar skýrslugerðar hefur stillt.

| Hlutverk (AOT-heiti)                     | Heiti hlutverks                                  | Skylda (AOT-heiti)                     | Heiti skyldu                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Þróunaraðili rafrænnar skýrslulausnar             | ERFormatDestinationConfigure        | Skilgreina viðtökustað rafræns skýrslugerðarsniðs                |
| ERFunctionalConsultant              | Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar | ERFormatDestinationConfigure        | Skilgreina viðtökustað rafræns skýrslugerðarsniðs                |
| PaymAccountsPayablePaymentsClerk    | Starfsmaður viðskiptaskuldagreiðslna            | ERFormatDestinationRuntimeConfigure | Skilgreina viðtökustað rafræns skýrslugerðarsniðs við keyrslu |
| PaymAccountsReceivablePaymentsClerk | Starfsmaður viðskiptakröfugreiðslna         | ERFormatDestinationRuntimeConfigure | Skilgreina viðtökustað rafræns skýrslugerðarsniðs við keyrslu |

> [!NOTE]
> Tvenn réttindi eru notaðar við fyrri störf. Þessi réttindi hafa sama heiti og samsvarandi skyldum: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Ég hef flutt inn rafræna skilgreiningar og ég sé þær á síðunni fyrir skilgreiningar Rafræna skýrslugerð. En af hverju sé ég ekki þær á síðu fyrir áfangastaði Rafrænnar skýrslugerðar?

Gangið úr skugga um að valið sé **Nýtt** og veldu síðan skilgreiningu í á **Tilvísun** svæði. Síðan **Áfangastaði Rafræna skýrslugerð** sýnir aðeins skilgreiningar sem áfangastaðir hafa verið skilgreind fyrir.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Er einhver leið til að skilgreina hvaða Microsoft Azure Geymslulykil og Azure Blob geymsla er notaður?

Nei. Sjálfgefna Microsoft Azure Blob geymslan sem er skilgreind og notað fyrir skjalastjórnunarkerfið er notað.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hver er tilgangur áfangastaðar skrár í stillingar fyrir áfangastað? Hvað gerir sú stillingu?

Áfangastaður **skráar** er notaður til að stjórna svarglugga vafrans þegar snið rafrænnar skýrslugerðar er keyrt í gagnvirkri stillingu. Ef þessi áfangastaður er virkjaður, eða ef enginn áfangastaður er skilgreindur fyrir skilgreiningu, sést svargluggi til að opna eða vista í vafranum eftir að úttaksskrá hefur verið búin til.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Er Hægt að veita dæmi um formúluna sem vísar til reikning lánardrottins sem ég get set tölvupóst til?

Athugið að formúlur eru sérstaklega ætlaðar fyrir skilgreiningu rafrænnar skýrslugerðar. Dæmi: Ef ISO 20022 skilgreining millifærslu fjármuna er notuð, **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** eða **líkan. Payments.Creditor.Identification.SourceID** til að fá lykill lánardrottins sem er tengd.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Einn af mínar skilgreiningar sniðs inniheldur margar skrár sem eru flokkaðar í einni möppu (t.d. Folder1 inniheldur File1, File2 og File3). Hvernig set ég upp áfangastaði þannig að Folder1.zip var ekki stofnuð yfir höfuð, File1 er send með tölvupósti, File2 er sent til SharePoint og ég get opnað File3 strax eftir skilgreining er keyrð?

Sniðið verður fyrst að vera tiltæk í skilgreiningum rafrænnar skýrslugerðar. Ef þessar forsendu er mætt skal opna síðuna **áfangastað Rafræn skýrslugerðar** og stofna ný tilvísun í þessa skilgreiningu. Síðan verður að hafa fjóra áfangastaði skráa , ein fyrir hvern frálagsíhlut. Stofna fyrsta ákvörðunarstað skrár , gefa því heiti eins og **Möppu**, og veljið skrárnafn sem táknar möppu í þinni skilgreiningu. Veldu síðan **Stillingar**, og gangið úr skugga um að allar áfangastaði eru óvirkir. Fyrir þessa áfangasta skrár, verður mappan ekki stofnuð. Að sjálfgefnu, vegna tengsla stigveldis milli skrár og yfirskipaðra mappa, munu skrárnar verða hegða sér á sama hátt. Með öðrum orðum þeir ekki verða sendir neitt. Til að hnekkja þeirri sjálfgefinni hegðun, verður að stofna þrjá fleiri áfangastaði skrár , einn fyrir hverja skrá. Í stillingum áfangastaðar fyrir hverja, þarf að virkja ákvörðunarstað sem á að senda skrána á.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Skilgreina áfangastaði rafrænnar skýrslugerðar sem eru háðir aðgerð](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
