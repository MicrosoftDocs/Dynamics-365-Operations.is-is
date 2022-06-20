---
title: Skilgreina rafræna skýrslugerð (ER) til að draga gögn inn í Power BI
description: Þessi grein útskýrir hvernig þú getur notað rafræna skýrslugerð (ER) stillingar þínar til að skipuleggja flutning gagna frá tilviki þínu til Power BI þjónusta.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6903513dec4da20dbc4463fbae6a406fc06e1a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896735"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Skilgreina rafræna skýrslugerð (ER) til að draga gögn inn í Power BI

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig þú getur notað rafræna skýrslugerð (ER) stillingar þínar til að skipuleggja flutning gagna frá tilviki þínu til Power BI þjónusta. Sem dæmi notar þessi grein Intrastat-færslur sem viðskiptagögn sem þarf að flytja. Myndræn útfærsla á korti Power BI notar þessi gögn intrastat-færslu til að birta greiningu á aðgerðum fyrirtækis varðandi inn- og útflutning á Power BI-skýrslu.

## <a name="overview"></a>Yfirlit

Microsoft Power BI er safn af þjónustu við hugbúnaðar, forritum og tengi sem vinna saman að því að breyta utanaðkomandi gögn í heildstæða, sjónrænar, og gagnvirka innsýn. Rafræna skýrslugerð (ER) gerir notendum kleift að skilgreina gagnagjafa auðveldlega og sjá um flutning gagna úr forritinu yfir í Power BI. Gögn eru flutt sem skrár á sniði OpenXML (Microsoft Excel vinnubókarskrá) vinnublaði. Fluttar skrárnar eru vistaðar í Microsoft SharePoint Server sem hefur verið skilgreindur fyrir þess háttar tilgang. Vistaðar skrár eru notaðar í Power BI til að gera skýrslur sem innihalda sjóræna birtingu (töflur gröf, varpanir og svo framvegis). Power BI skýrslum er deilt með Power BI notendum og þær eru opnaðar í Power BI-yfirlitum og á síðum forritsins. Þessi grein útskýrir eftirfarandi verkefni:

- Stilla Microsoft Dynamics 365 Fjármál.
- Undirbúðu ER sniðsskilgreiningu þína fyrir móttöku gagna úr Finance-forritinu.
- Skilgreina umhverfi Rafræn skýrslugerðar til að flytja gögn í Power BI.
- Nota flutt gögn til að stofna Power BI-skýrsla.
- Gerðu Power BI-skýrsluna aðgengilega í Finance.

## <a name="prerequisites"></a>Forkröfur
Til að klára dæmið í þessari grein verður þú að hafa eftirfarandi aðgang:

- Aðgengi fyrir eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Aðgangur að SharePoint-þjóni sem er grunnstillt til notkunar með forritinu.
- Aðgangur að Power BI-rammanum

## <a name="configure-document-management-parameters"></a>Skilgreina færibreytur skjalastjórnunar
1. Á **Færibreytur skjalastjórnunar** síðunni, skilgreina aðgangur að SharePoint Server sem verður notuð í fyrirtækinu sem þú ert skráður inn í (DEMF í þessu dæmi).
2. Prófa tengingu við SharePoint Server til að tryggja að þú höfum verið veittur aðgangur.

    [![Síðan Færibreytur skjalastjórnunar.](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Opnið skilgreinda SharePoint svæðið. Stofna nýja möppu þar sem Rafræn skýrslugerð mun vista Excel-skrár sem hafa viðskiptagögn sem Power BI-skýrslur krefjast sem uppruna gagnasafna Power BI.
4. Á síðunni **Skjalagerðir** stofnarðu nýja gerð skjala sem verður notuð til að fá aðgang að SharePoint-möppu sem nýverið var stofnuð. Færið inn **Skrá** í **Hópur** svæðinu og **SharePoint** í **Staðsetningu** svæðinu og færa svo inn aðsetur SharePoint-möppu.

    [![Síða skjalategunda.](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar
1. Í á **Rafrænnar skýrslugerðar** vinnusvæði, smellið á **færibreytur Rafræna skýrslugerðar** tengil.
2. Á **Viðhengi** flipanum, veljið á **Skrá** skjalagerð fyrir öll svæði.
3. Í á **Rafræna skýrslugerð** vinnusvæði, gerið nauðsynlegan veitanda virkan með því að smella á **gera virkan**. Nánari upplýsingar má fá með því að spila **Rafræn skýrslugerð velja þjónustuveitu** leiðarvísi fyrir verk.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Nota skal gagnalíkan rafrænnar skýrslugerðar sem uppruna gagna.
Nota skal gagnalíkan rafrænnar skýrslugerðar sem uppruna gagna sem verður notaður í Power BI-skýrslur. Þessi gagnalíkan er hlaðið upp úr skilgreiningagagnasafni rafrænnar skýrslugerðar. Nánari upplýsingar, sjá [Sækja skilgreiningar rafrænnar skýrslugerðar frá Lifecycle Services](download-electronic-reporting-configuration-lcs.md), eða spila **Rafræn skýrslugerð flytja inn skilgreiningu úr Lifecycle Services** leiðarvísi fyrir verk. Veljið **Intrastat** sem gagnalíkan sem hlaðið verður upp úr valinni skilgreiningagagnasafni rafrænnar skýrslugerðar. (Í þessu dæmi er útgáfa 1 af líkaninu notuð.) Svo er hægt að fara á **Intrastat** skilgreiningu líkans fyrir rafræna skýrslugerð á síðunni **Skilgreiningar**.

[![Intrastat skilgreiningarlíkan rafrænnar skýrslugerðar á skilgreiningarsíðunni.](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Hanna skilgreiningu fyrir snið rafrænnar skýrslugerðar
Þú þarft að stofna nýtt skilgreiningu sniðs rafrænnar skýrslugerðar sem notar **Intrastat** gagnalíkan sem gagnagjafi viðskiptagagna. Þessa sniðsskilgreiningu verður að mynda niðurstöður úttaks sem rafræn skjöl á OpenXML (Excel-skrá) sniði. Til að fá frekari upplýsingar skaltu Spila **ER stofna skilgreiningu fyrir skýrslur í OPENXML-sniði** leiðarvísi fyrir verk. Nefndu nýja skilgreiningu **aðgerðir Innflutnings / útflutnings**, eins og sýnt er í eftirfarandi dæmi. Notaðu [gögn rafrænnar skýrslugerðar - upplýsingar um innflutning og útflutning](https://download.microsoft.com/download/f/7/5/f755c0fd-025c-4aa9-920b-909abb8302ad/ER-data-import-and-export-details.xlsx) Excel-skrá sem sniðmát þegar sniðið rafrænnar skýrslugerðar er hönnuð. (Upplýsingar um hvernig á að flytja inn sniðmát sniðs, spila leiðarvísi fyrir verk.)

[![Skilgreining á aðgerðum innflutnings/útflutnings.](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

Til að breyta skilgreiningu sniðs **aðgerðum innflutnings/útflutnings**, skal fylgja þessum skrefum.

1. Smellið á **Hönnuður**.
2. Á **Snið** flipanum, nefdu skráreininguna fyrir þetta **skrá fyrir Excel-úttak** snið.

    [![Skráareining fyrir Excel-úttak.](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. Á **Vörpun** flipanum skal tilgreina heiti Excel-skráin sem verður myndað í hvert sinn sem þetta snið er keyrð. Skilgreinið tengdar segð til að skila gildi **upplýsingar um Innflutning og útflutning** (.xlsx skrárending verður bætt við sjálfkrafa).

    [![Sniðshönnuður.](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Bætið við nýja afurð gagnagjafa fyrir þetta snið. (Þessi tölusetning er nauðsynleg fyrir frekari gagnabindingu.)

    1. Nefndu gagnagjafann **direction\_enum**.
    2. Veljið **tölusetning gagnalíkans** sem gerð gagnagjafa.
    3. Vísað er tölusetningu gagnalíkans **Stefna**.

    [![direction_enum.](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. Ljúka bindingu eininga á **Intrastat** gagnalíkani og einingum hins hannaða sniðs, sem sýna í eftirfarandi dæmi.

    [![Ljúka við bindingu.](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Eftir að hún er keyrð myndar snið rafrænnar skýrslugerðar niðurstöður úttaks á Excel-sniði. Hann sendir upplýsingar um intrastat-færslur í niðurstöður úttaks og aðskilur þær sem færslur sem lýsa annaðhvort verkþætti innflutnings eða útflutnings. Smelltu á **Keyra** til að prófa nýja snið rafrænnar skýrslugerðar fyrir lista yfir Intrastat-færslur á síðunni **Intrastat** (**Skattur** &gt; **Skattskýrslur** &gt; **Erlend viðskipti** &gt; **Intrastat**).

[![Intrastat-síða.](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Eftirfarandi niðurstaða úttaks er mynduð. Skráin er með heitinu **upplýsingar um Innflutningur og útflutningur.xlsx**, eins og tilgreint er í stillingum sniðs.

[![Upplýsingar um innflutning og útflutning.xlsx.](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Skilgreina áfangastað Rafræn skýrslugerðar
Þú verður að Skilgreina ramma rafrænnar skýrslugerðar til að senda niðurstaða úttaks nýrrar skilgreiningar sniðs rafrænnar skýrslugarðar á sérstakan hátt.

- Senda þarf niðurstöður úttaks í möppu hins valda SharePoint Server.
- Hver keyrsla skilgreiningarsniðs þarf að stofna nýja útgáfu sama Excel-skrá.

Á síðunni **Rafræn skýrslugerð** (**Fyrirtækisstjórnun** &gt; **Rafræn skýrslugerð**) er smellt á atriðið **Viðtökustaður rafrænnar skýrslugerðar** og bætt við nýjum viðtökustað. Í **Tilvísun** svæðinu, veljið **Aðgerðir Innflutnings / útflutnings** skilgreiningarsnið sem stofnaðar voru áður. Fylgið eftirfarandi skrefum til að bæta við nýrri færslu fyrir áfangastað skrár fyrir tilvísunina.

1. Í **Heiti** svæðinu, færið inn heiti áfangastaðar skrár.
2. Á **skrárheiti** svæðinu skal velja nafn **Excel-skrár fyrir úttak** fyrir íhlut Excel-skráarsniðs.

Smellið á **Stillingar** hnappinn fyrir nýja færslu áfangastaðar. Síðan, í **stillingar fyrir Áfangastað** svarglugganum, skal fylgja þessum skrefum.

1. Á **Power BI** flipanum, skal stilla **Virkjaðar** valkosturinn á **Já**.
2. Á **SharePoint** svæðinu, veljið þá **Samnýttum** skjalagerð sem þú stofnaðir áður.

## <a name="schedule-execution-of-the-configured-er-format"></a>Áætla framkvæmd á skilgreindu sniði rafrænnar skýrslugerðar
1. Á síðunni **Skilgreiningar** (**Fyrirtækisstjórnun** &gt; **Rafræn skýrslugerð** &gt; **Skilgreiningar**), í grunnstillingatrénu, skal velja skilgreininguna **Aðgerðir innflutnings/útflutnings** sem stofnuð var áður.
2. Breyta stöðu útgáfu 1.1 úr **Drög** að **Lokið** til að gera þessi snið tiltækar.

    [![Skilgreining inn-/útflutningsaðgerða á skilgreiningarsíðunni.](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. Veljið lokna útgáfu skilgreiningarinnar **aðgerðir Innflutnings / útflutnings** og smelltu svo á **Keyra**. Athugið að skilgreindur áfangastaður notaður fyrir niðurstöður úttaks sem er mynduð í Excel-sniði.
4. Setja **runuvinnslu** valkosturinn að **Já** til að keyra þessa skýrslu í fjarveruham.
5. Smellið á **Endurtekningar** til að áætla nauðsynlegar endurtekningar í framkvæmdar þessarar runu. Endurtekningin tilgreinir hversu oft uppfærð gögn verða fluttar yfir í Power BI.

    [![Svargluggi rafrænna skýrslufæribreyta.](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Eftir að hún er skilgreind er hægt að finna vinnsluverk skýrslu rafrænnar skýrslugerðar á síðunni **Runuvinnslur** (**Kerfisstjórnun &gt; Fyrirspurnir &gt; Runuvinnslur**).

    [![Síða runuvinnslu.](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Þegar þessi vinnsla er keyrð í fyrsta sinn, stofnar áfangastað nýja excel-skrá sem hefur skilgreinda heiti í völdu SharePoint-möppunni . Hvert síðari skipti sem vinnslan er keyrð, stofnar áfangastaðurinn nýja útgáfu Excel-skráarinnar.

    [![Ný útgáfa Excel-skráar.](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Stofna Power BI-gagnasafn með því að nota niðurstöðu úttaks sniðs rafrænnar skýrslugerðar
1. Innskráning í Power BI og annaðhvort opna fyrirliggjandi Power BI-flokk (vinnusvæði) eða stofnið nýjan flokk. Annaðhvort smella á **Bæta við** undir **Skrár** í **Flytja inn eða tengjast gögnum** hlutanum eða smella á plúsmerkið (**+**) við hliðina á **Gagnasöfn** í vinstri glugganum.

    [![Gagnasafn stofnað.](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. Velja skal valkostinn **SharePoint – Teymasvæði** og færa síðan inn slóð SharePoint-þjóns sem verið er að nota (`https://ax7partner.litware.com` í okkar dæmi).
3. Flettið að möppunni **/Shared Documents/GER data/PowerBI** og veljið Excel-skrána sem var stofnuð sem gagnagjafi fyrir nýja Power BI gagnasafnið.

    [![Velja Excel-skrá.](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. Smellið á **tengja** og smellið síðan á **Flytja inn**: Ný gagnasafn er stofnað sem byggir á völdum Excel-skrá. Dataset má einnig bæta við sjálfkrafa við nýlega stofnað yfirlit.

    [![Gagnasafn á yfirliti.](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Skilgreina uppfærsluáætlun fyrir þessa gagnasafnið sem á að láta uppfæra reglubundið. Reglulegar uppfærslur virkja notkun nýtt viðskiptagögn sem koma gegnum reglubundna keyrslu skýrslu rafrænnar skýrslugerðar gegnum nýjar útgáfur af Excel-skráin sem eru stofnuð á SharePoint-þjóni.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Stofna Power BI skýrslu með því að nota nýja gagnasafnið.
1. Smellið á **Upplýsingar um inn- og útflutning** Power BI gagnasafnið sem var stofnað.
2. Skilgreinið myndrænu framsetninguna. Veljið til dæmis á **Útfyllt korti** myndræn útfærsla, og skilgreina sem hér segir:

    - Úthluta skal **CountryOrigin** svæði gagnasafns til **Staðsetningu** svæðinu í myndræn útfærsla korts.
    - Úthluta skal **upphæð** svæði gagnasafns til **litamettun** svæðinu í myndræn útfærsla korts.
    - Bæta við **Aðgerð** og **Ár** svlpu gagnasafns í **Síur** safni svæða í myndræn útfærsla korts.

3. Vista Power BI-skýrsla sem **skýrslu með upplýsingum um Innflutning og útflutning**.

    [![Skýrsla með upplýsingum um innflutning og útflutning.](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Athugið að vörpunin sýnir lönd/svæði sem nefnd eru í Excel-skrá (Austurríki og Sviss í þessu dæmi). Þessum lönd/svæði eru litaða til að sýna hlutfalli á reikningsfærðar upphæðir fyrir hvert.

4. Uppfæra listann yfir Intrastat-færslur. Útflutningsfærslan sem á uppruna sinn á Ítalíu er bætt við.

    [![Listi yfir Intrastat-færslur.](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. Bíða eftir næstu áætluðu keyrsla skýrslu rafrænnar skýrslugerðar og næsta áætlaða uppfærsla Power BI-gagnasafn. Yfirfara svo Power BI-skýrslu (velja að birta aðeins innflutningsfærslur) . Uppfært kort sýnir nú Ítalía.

    [![Uppfært kort.](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance"></a>Aðgangur Power BI-skýrslu í Finance
Setja upp samþættingu við Power BI. Nánari upplýsingar, sjá [Skilgreina samþættingu Power BI fyrir vinnusvæði](configure-power-bi-integration.md).

1. Á vinnusvæðissíðunni **Rafræn skýrslugerð** sem styður samþættingu Power BI (**Fyrirtækisstjórnun** &gt; **Vinnusvæði** &gt; **Vinnusvæði rafrænnar skýrslugerðar**) skal smella á **Valkostir** &gt; **Opna skýrslulista**.
2. Velja skal **Upplýsingar um Innflutning og útflutning** Power BI skýrsluna sem þú stofnaðir, til að sýna þá skýrslu sem aðgerðaratriði á valinni síðu.
3. Smellt er á vöru til að opna síðuna sem sýnir skýrslan sem þú hannaðir í Power BI.

    [![Skýrsla með upplýsingum um innflutning og útflutning hönnuð í Power BI.](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)

[Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
