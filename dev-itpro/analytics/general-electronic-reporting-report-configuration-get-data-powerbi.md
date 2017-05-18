---
title: "Skilgreina Rafræna skýrslugerð til að draga gögn inn í Power BI"
description: "Þessu efnisatriði útskýrir hvernig nota skal skilgreiningu Rafræna skýrslugerðar (ER) til að sjá um flutning gagna úr tilviki Dynamics 365 for Operations til Power BI-þjónustu. Sem dæmi, notar þessa efnisatriðis intrastat-færslur sem viðskiptagögn sem verður að flytja. Myndræn útfærsla á korti Power BI notar þessi gögn intrastat-færslu til að birta greiningu á aðgerðum fyrirtækis varðandi inn- og útflutning á Power BI-skýrslu."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 4bbc77eb1edfe0c109434ce4d26228ed031f48bc
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="configure-electronic-reporting-to-pull-data-into-power-bi"></a>Skilgreina Rafræna skýrslugerð til að draga gögn inn í Power BI

[!include[banner](../includes/banner.md)]


Þessu efnisatriði útskýrir hvernig nota skal skilgreiningu Rafræna skýrslugerðar (ER) til að sjá um flutning gagna úr tilviki Dynamics 365 for Operations til Power BI-þjónustu. Sem dæmi, notar þessa efnisatriðis intrastat-færslur sem viðskiptagögn sem verður að flytja. Myndræn útfærsla á korti Power BI notar þessi gögn intrastat-færslu til að birta greiningu á aðgerðum fyrirtækis varðandi inn- og útflutning á Power BI-skýrslu.

<a name="overview"></a>Yfirlit
--------

Microsoft Power BI er safn af þjónustu við hugbúnaðar, forritum og tengi sem vinna saman að því að breyta utanaðkomandi gögn í heildstæða, sjónrænar, og gagnvirka innsýn. Rafræna skýrslugerð (ER) gerir notendum Microsoft Dynamics 365 for Operations kleift að skilgreina gagnagjafa auðveldlega og sjá um flutning gagna úr Dynamics 365 for Operations yfir í Power BI. Gögn eru flutt sem skrár á sniði OpenXML (Microsoft Excel vinnubók skrá) vinnublaði. Fluttar skrárnar eru vistaðar í Microsoft SharePoint Server sem hefur verið skilgreindur fyrir þess háttar tilgang. Vistaðar skrár eru notaðar í Power BI til að gera skýrslur sem innihalda sjóræna birtingu (töflur gröf, varpanir og svo framvegis). Power BI skýrslur eru deilt með Power BI notendur og þeir eru opnuð í Power BI-yfirlitum og á síðum Dynamics 365 for Operations. Efnisatriðið útskýrir eftirfarandi Verkhlutar:

-   Skilgreina Dynamics 365 for Operations.
-   Undirbúa skilgreiningu sniðs rafrænnar skýrslugerðar til að fá gögn úr Dynamics 365 for Operations.
-   Skilgreina umhverfi Rafræn skýrslugerðar til að flytja gögn í Power BI.
-   Nota flutt gögn til að stofna Power BI-skýrsla.
-   Gera skýrslu Power BI aðgengilega í Dynamics 365 for Operations.

## <a name="prerequisites"></a>Forkröfur
Til að ljúka dæminu í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:

-   Aðgangi til Dynamics 365 for Operations fyrir einn eftirfarandi hlutverk:
    -   Þróunaraðili rafrænnar skýrslulausnar
    -   Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    -   Kerfisstjóri
-   Aðgangur að SharePoint Server sem er skilgreint til notkunar með Dynamics 365 for Operations.
-   Aðgangi að Power BI-ramma

## <a name="configure-document-management-parameters"></a>Skilgreina færibreytur skjalastjórnunar
1.  Á **Færibreytur skjalastjórnunar** síðunni, skilgreina aðgangur að SharePoint Server sem verður notuð í fyrirtækinu sem þú ert skráður inn í (DEMF í þessu dæmi).
2.  Prófa tengingu við SharePoint Server til að tryggja að þú höfum verið veittur aðgangur. [![Síðan Færibreytur skjalastjórnunar](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Opna skilgreinda SharePoint-svæði. Stofna nýja möppu þar sem Rafræn skýrslugerð mun vista Excel-skrár sem hafa viðskiptagögn sem Power BI-skýrslur krefjast sem uppruna gagnasafna Power BI.
4.  Í Dynamics 365 for Operations á í **Skjalagerðir** síðunni, stofna nýja gerð skjala sem verða notaðir til að fá aðgang að SharePoint-möppu sem nýverið var stofnuð. Færið inn **Skrá** í á **Flokk** svæðinu og **SharePoint** í á **Staðsetningu** svæðinu og færa svo inn aðsetur SharePoint-möppu. [![Síðan Gerðir skjala](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar
1.  Í á **Rafrænnar skýrslugerðar** vinnusvæði, smellið á **færibreytur Rafræna skýrslugerðar** tengil.
2.  Á **Viðhengi** flipanum, veljið á **Skrá** skjalagerð fyrir öll svæði.
3.  Í á **Rafræna skýrslugerð** vinnusvæði, gerið nauðsynlegan veitanda virkan með því að smella á **gera virkan**. Nánari upplýsingar má fá með því að spila **Rafræn skýrslugerð velja þjónustuveitu** leiðarvísi fyrir verk.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Nota skal gagnalíkan rafrænnar skýrslugerðar sem uppruna gagna.
Nota skal gagnalíkan rafrænnar skýrslugerðar sem uppruna gagna sem verður notaður í Power BI-skýrslur. Þessi gagnalíkan er hlaðið upp úr skilgreiningagagnasafni rafrænnar skýrslugerðar. Nánari upplýsingar, sjá [Sækja skilgreiningar rafrænnar skýrslugerðar frá Lifecycle Services](download-electronic-reporting-configuration-lcs.md), eða spila **Rafræn skýrslugerð flytja inn skilgreiningu úr Lifecycle Services** leiðarvísi fyrir verk. Veljið **Intrastat** sem gagnalíkan sem hlaðið verður upp úr valinni skilgreiningagagnasafni rafrænnar skýrslugerðar. (Í þessu dæmi er útgáfa 1 af líkaninu notuð.) Svo er hægt að fara á **Intrastat** skilgreiningu líkans fyrir rafræna skýrslugerð á síðunni **Skilgreiningar**. [![Skilgreiningasíða](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Hanna skilgreiningu fyrir snið rafrænnar skýrslugerðar
Þú þarft að stofna nýtt skilgreiningu sniðs rafrænnar skýrslugerðar sem notar **Intrastat** gagnalíkan sem gagnagjafi viðskiptagagna. Þessa sniðsskilgreiningu verður að mynda niðurstöður úttaks sem rafræn skjöl á OpenXML (Excel-skrá) sniði. Til að fá frekari upplýsingar skaltu Spila **ER stofna skilgreiningu fyrir skýrslur í OPENXML-sniði** leiðarvísi fyrir verk. Nefndu nýja skilgreiningu **aðgerðir Innflutnings / útflutnings**, eins og sýnt er í eftirfarandi dæmi. Notaðu [gögn rafrænnar skýrslugerðar - upplýsingar um innflutning og útflutning](https://go.microsoft.com/fwlink/?linkid=845208) Excel-skrá sem sniðmát þegar sniðið rafrænnar skýrslugerðar er hönnuð. (Upplýsingar um hvernig á að flytja inn sniðmát sniðs, spila verkefnaleiðbeiningar.) [![Skilgreining á aðgerðum innflutnings/útflutnings](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) til að breyta skilgreiningu sniðsins **Aðgerðir innflutnings/útflutnings** skal gera eftirfarandi.

1.  Smellið á **Hönnuður**.
2.  Á **Snið** flipanum, nefdu skráreininguna fyrir þetta **skrá fyrir Excel-úttak** snið. [![Skráreining fyrir Excel-úttak](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  Á **Vörpun** flipanum skal tilgreina heiti Excel-skráin sem verður myndað í hvert sinn sem þetta snið er keyrð. Skilgreinið tengdar segð til að skila gildi **upplýsingar um Innflutning og útflutning** (.xlsx skrárending verður bætt við sjálfkrafa). [![Sniðshönnuður](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Bætið við nýja afurð gagnagjafa fyrir þetta snið. (Þessi tölusetning er nauðsynleg fyrir frekari gagnabindingu.)
    1.  Nefndu gagnagjafann **direction\_enum**.
    2.  Veljið **tölusetning gagnalíkans** sem gerð gagnagjafa.
    3.  Vísað er tölusetningu gagnalíkans **Stefna**.

    [![direction\_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Ljúka bindingu eininga á **Intrastat** gagnalíkani og einingum hins hannaða sniðs, sem sýna í eftirfarandi dæmi. [![Ljúka við bindingu](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Eftir að hún er keyrð myndar snið rafrænnar skýrslugerðar niðurstöður úttaks á Excel-sniði. Hann sendir upplýsingar um intrastat-færslur í niðurstöður úttaks og aðskilur þær sem færslur sem lýsa annaðhvort verkþætti innflutnings eða útflutnings. Smelltu á **Keyra** til að prófa nýja snið rafrænnar skýrslugerðar fyrir lista yfir Intrastat-færslur á síðunni **Intrastat** (**Skattur** &gt; **Skattskýrslur** &gt; **Erlend viðskipti** &gt; **Intrastat**). [![Intrastat-síða](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) Eftirfarandi niðurstaða úttaks er mynduð. Skráin er með heitinu **upplýsingar um Innflutningur og útflutningur.xlsx**, eins og tilgreint er í stillingum sniðs. [![Upplýsingar um innflutning og útflutning.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Skilgreina áfangastað Rafræn skýrslugerðar
Þú verður að Skilgreina ramma rafrænnar skýrslugerðar til að senda niðurstaða úttaks nýrrar skilgreiningar sniðs rafrænnar skýrslugarðar á sérstakan hátt.

-   Senda þarf niðurstöður úttaks í möppu hins valda SharePoint-þjóns.
-   Hver keyrsla skilgreiningarsniðs þarf að stofna nýja útgáfu sama Excel-skrá.

Á síðunni **Rafræn skýrslugerð** (**Fyrirtækisstjórnun** &gt; **Rafræn skýrslugerð**) er smellt á atriðið **Viðtökustaður rafrænnar skýrslugerðar** og bætt við nýjum viðtökustað. Í **Tilvísun** svæðinu, veljið **Aðgerðir Innflutnings / útflutnings** skilgreiningarsnið sem stofnaðar voru áður. Fylgið eftirfarandi skrefum til að bæta við nýrri færslu fyrir áfangastað skrár fyrir tilvísunina.

1.  Í **Heiti** svæðinu, færið inn heiti áfangastaðar skrár.
2.  Á **skrárheiti** svæðinu skal velja nafn **Excel-skrár fyrir úttak** fyrir íhlut Excel-skráarsniðs.

Smellið á **Stillingar** hnappinn fyrir nýja færslu áfangastaðar. Síðan, í **stillingar fyrir Áfangastað** svarglugganum, skal fylgja þessum skrefum.

1.  Á **Power BI** flipanum, skal stilla **Virkjaðar** valkosturinn á **Já**.
2.  Á **SharePoint** svæðinu, veljið þá **Samnýttum** skjalagerð sem þú stofnaðir áður.

## <a name="schedule-execution-of-the-configured-er-format"></a>Áætla framkvæmd á skilgreindu sniði rafrænnar skýrslugerðar
Á síðunni **Skilgreiningar** (**Fyrirtækisstjórnun** &gt; **Rafræn skýrslugerð** &gt; **Skilgreiningar**), í grunnstillingatrénu, skal velja skilgreininguna **Aðgerðir innflutnings/útflutnings** sem stofnuð var áður. Breyta stöðu útgáfu 1.1 úr **Drög** að **Lokið** til að gera þessi snið tiltækar. [![Skilgreiningasíða](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) Veljið lokna útgáfu skilgreiningarinnar **Aðgerðir innflutnings/útflutnings** og smellið svo á **Keyra**. Athugið að skilgreindur áfangastaður notaður fyrir niðurstöður úttaks sem er mynduð í Excel-sniði. Setja **runuvinnslu** valkosturinn að **Já** til að keyra þessa skýrslu í fjarveruham. Smellið á **Endurtekningar** til að áætla nauðsynlegar endurtekningar í framkvæmdar þessarar runu. Endurtekningin tilgreinir hversu oft uppfærð gögn verða fluttar úr Dynamics 365 for Operations yfir í Power BI. [![Svarglugginn Rafrænar skýrslufæribreytur](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) Eftir að hún er skilgreind er hægt að finna vinnsluverk skýrslu rafrænnar skýrslugerðar á síðunni **Runuvinnslur** (**Kerfisstjórnun &gt; Fyrirspurnir &gt; Runuvinnslur**). [![Síðan Runuvinnslur](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) Þegar þessi vinnsla er keyrð í fyrsta sinn stofnar viðtökustaðurinn nýja Excel-skrá sem hefur skilgreinda heitið í völdu SharePoint-möppunni. Hvert síðari skipti sem vinnslan er keyrð, stofnar áfangastaðurinn nýja útgáfu Excel-skráarinnar. [![Ný útgáfa Excel-skrár](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Stofna Power BI-gagnasafns með því að nota niðurstöðu úttaks sniðs rafrænnar skýrslugerðar.
Innskráning í Power BI og annaðhvort opna fyrirliggjandi Power BI-flokk (vinnusvæði) eða stofnið nýjan flokk. Annaðhvort smella á **Bæta við** undir **Skrár** í **Flytja inn eða tengjast gögnum** hlutanum eða smella á plúsmerkið (**+**) við hliðina á **Gagnasöfn** í vinstri glugganum. [![Gagnasafn stofnað](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) Velja skal **SharePoint – teymasvæði** valkostinn og færa síðan inn slóð SharePoint-þjóns sem verið er að nota (**https://ax7partner.spoppe.com** í okkar dæmi). Flettið síðan að **/Shared Documents/GER data/PowerBI**-möppu og veljið Excel-skráin sem var stofnuð sem gagnagjafa fyrir ný Power BI-gagnasafn. [![Excel-skrá valin](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) Smellið á **Tengja** og síðan á **Innflutningur**. Ný gagnasafn er stofnað sem byggir á völdum Excel-skrá. Dataset má einnig bæta við sjálfkrafa við nýlega stofnað yfirlit. [![Gagnasafn á yfirliti](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) Skilgreina uppfærsluáætlun fyrir þetta gagnasafn til að láta uppfæra reglubundið. Reglulegar uppfærslur virkja notkun nýtt viðskiptagögn sem koma úr Dynamics 365 for Operations gegnum reglubundna keyrslu skýrslu rafrænnar skýrslugerðar gegnum nýjar útgáfur af Excel-skráin sem eru stofnuð á SharePoint-þjóni.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Stofna Power BI skýrslu með því að nota nýja gagnasafnið.
Til að stofna nýja Power BI skýrslu skal smellt á í **upplýsingar um Innflutning og útflutning** Power BI-gagnasafn sem þú stofnaðir. Svo skal Skilgreina myndræn útfærsla. Veljið til dæmis á **Útfyllt korti** myndræn útfærsla, og skilgreina sem hér segir:

-   Úthluta skal **CountryOrigin** svæði gagnasafns til **Staðsetningu** svæðinu í myndræn útfærsla korts.
-   Úthluta skal **upphæð** svæði gagnasafns til **litamettun** svæðinu í myndræn útfærsla korts.
-   Bæta við **Aðgerð** og **Ár** svlpu gagnasafns í **Síur** safni svæða í myndræn útfærsla korts.

Vista Power BI-skýrsla sem **skýrslu með upplýsingum um Innflutning og útflutning**. [![Skýrsla með upplýsingum um innflutning og útflutning](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Athugið að kortið sýnir lönd/svæði sem nefnd eru í Excel-skránni (Austurríki og Sviss í þessu dæmi). Þessum lönd/svæði eru litaða til að sýna hlutfalli á reikningsfærðar upphæðir fyrir hvert. Uppfæra listann yfir Intrastat-færslur. Útflutningsfærslan sem á uppruna sinn á Ítalíu er bætt við. [![Listi yfir Intrastat-færslur](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) Bíða eftir næstu áætluðu keyrslu skýrslu rafrænnar skýrslugerðar og næstu áætluðu uppfærslu Power BI-gagnasafns. Yfirfara svo Power BI-skýrslu (velja að birta aðeins innflutningsfærslur) . Uppfært kort sýnir nú Ítalía. [![Uppfært kort](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Opna Power BI-skýrslu í Dynamics 365 for Operations.
Setja upp samþættingu á milli Power BI og Dynamics 365 for Operations. Nánari upplýsingar, sjá [Skilgreining samþættingar Power BI fyrir vinnusvæði](configure-power-bi-integration.md). Á vinnusvæðissíðunni **Rafræn skýrslugerð** sem styður samþættingu Power BI (**Fyrirtækisstjórnun** &gt; **Vinnusvæði** &gt; **Vinnusvæði rafrænnar skýrslugerðar**) skal smella á **Valkostir** &gt; **Opna skýrslulista**. Velja skal Power BI-skýrsluna **upplýsingar um Innflutning og útflutning** sem þú stofnaðir, til að sýna þá skýrslu sem aðgerðaratriði á valinni síðu. Smellt er á vöru til að opna Dynamics 365 for Operations síðu sem sýnir skýrslan sem þú hannaðir í Power BI. [![Skýrsla með upplýsingum um innflutning og útflutning](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Sjá einnig
--------

[Viðtökustaður rafrænnar skýrslugerðar](electronic-reporting-destinations.md)

[Yfirlit yfir Rafræna skýrslugerð](general-electronic-reporting.md)




