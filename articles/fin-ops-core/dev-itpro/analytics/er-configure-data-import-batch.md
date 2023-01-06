---
title: Flytja inn gögn úr skrám sem voru valdar handvirkt í runustillingu
description: Þessi grein útskýrir flutning gagna úr skrám sem voru valdar handvirkt í runustillingu
author: kfend
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
ms.openlocfilehash: 21a2ab5f0eb07dda92baf9cc04ee36caeff8b4ec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288229"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Flytja inn gögn úr skrám sem voru valdar handvirkt í runustillingu

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Til að nota rammann [Rafræn skýrslugerð](general-electronic-reporting.md) til að flytja inn gögn úr handvirkt völdum skrám á innleið í runustillingu skal skilgreina [snið](er-overview-components.md#format-component) rafrænnar skýrslugerðar sem styður innflutninginn. Keyrðu síðan [líkanavörpun](er-overview-components.md#model-mapping-component) af gerðinni **Til endastaðar** sem notar það snið sem gagnagjafa. Til að flytja inn gögn skal fletta á skrána sem þú vilt flytja inn og velja hana handvirkt. 

Nýi möguleiki rafrænnar skýrslugerðar sem styður gagnainnflutning í runustillingu virkjar þetta ferli til að vera skilgreint sem eftirlitslaust. Hægt er að nota skilgreiningar rafrænnar skýrslugerðar til að framkvæma gagnainnflutning með því að tímasetja nýja runuvinnslu úr notendaviðmóti rafrænnar skýrslugerðar.

Þessi grein útskýrir hvernig á að ljúka gagnainnflutningi úr handvirkt valdri skrá í runustillingu. Dæmin nota lánardrottnafærslur sem viðskiptagögn. Hægt er að ljúka skrefunum þessara dæma í fyrirtækinu **USMF**. Ekki er þörf á neinni kóðun.

## <a name="prerequisites"></a>Forkröfur

Til að ljúka dæmunum í þessari grein þarftu að hafa eftirfarandi aðgang:

- Eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- ER snið og grunnstillingar líkans fyrir 1099 greiðslur

### <a name="create-the-required-er-configurations"></a>Búðu til nauðsynlegar skilgreining rafrænnar skýrslugerðar

Til að búa til nauðsynlegar skilgreiningar rafrænnar skýrslugerðar og fá önnur skilyrði skal fylgja einu af þessum skrefum:

- Spila **ER flytja inn gögn úr Microsoft Excel skrá** verkefnaleiðbeiningar, sem eru hluti af **7.5.4.3 Fá/Þróa upplýsingatækniþjónustu/lausn íhlutir (10677)** viðskiptaferli. Þessar verkefnaleiðbeiningar fylgja þér í gegnum ferlið við að hanna og nota ER grunnstillingar til að flytja inn lánardrottnafærslur á gagnvirkan máta frá Microsoft Excel skrám. Nánari upplýsingar er að finna í [Þátta skjöl á innleið á Excel-sniði](parse-incoming-documents-excel.md).
- Ljúka dæmunum í [Skilgreina gagnainnflutning úr SharePoint](er-configure-data-import-sharepoint.md). Þessi dæmi fylgja þér í gegnum ferlið við að hanna og nota ER grunnstillingar til að flytja inn lánardrottnafærslur á gagnvirkan máta frá Excel-skrám sem eru vistaðar í möppunni SharePoint.

### <a name="download-the-required-er-configurations"></a>Sækja nauðsynlegar skilgreining rafrænnar skýrslugerðar

1. Sæktu eftirfarandi skilgreiningar rafrænnar skýrslugerðar og vistaðu þær staðbundið.

    | Lýsing á efni | Skrá |
    |---------------------|------|
    | **1099 Greiðslulíkan** Skilgreining gagnalíkans rafrænnar skýrslugerðar | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | Skilgreining sniðs rafrænnar skýrslugerðar **Fyrir innflutning lánardrottnafærslna (Excel)** | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Notaðu valkostinn [Hlaða úr XML-skrá](er-defer-sequence-element.md#import-the-sample-er-configurations) fyrir rafræna skýrslugerð til að flytja inn sóttar skilgreiningar rafrænnar skýrslugerðar í tilvikið þitt af Dynamics 365 Finance í eftirfarandi röð:

    1. Skilgreining á gagnalíkani í ER
    2. ER Sníða skilgreiningu

### <a name="download-the-required-excel-files"></a>Sækja nauðsynlegar Excel-skrár

- Sæktu eftirfarandi sýnigagnasafn og vistaðu það á staðbundið.

    | Lýsing á efni | Skrá |
    |---------------------|------|
    | **1099import-data.xlsx** skrá á innleið sem inniheldur sýnigögn fyrir innflutning | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Fara yfir skilyrði

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar** skal fara yfir undirbúna lausn rafrænnar skýrslugerðar fyrir gagnainnflutning í runustillingu.
3. Farðu yfir sniðsskilgreininguna **Fyrir innflutning lánardrottnafærslna (Excel)**.

    - Sniðsþáttur þessarar skilgreiningar er hannaður til að þátta Excel-skrá á innleið.
    - Þáttur líkanavörpunar fyrir þessa skilgreiningu er notaður til að fylla út í grunngagnalíkanið með því að nota gögn úr þáttaðri Excel-skrá.

    ![Skilgreining sniðs rafrænnar skýrslugerðar fyrir innflutning gagna í runustillingu úr viðmóti rafrænnar skýrslugerðar.](./media/er-configure-data-import-batch-configurations-1.png)

4. Farðu yfir **1099 Greiðslulíkan** skilgreining gagnalíkans

    - Líkanaþáttur þessarar skilgreiningar stendur fyrir skipulag gagnalíkansins sem er notað til að flytja gögn á milli rafrænna skýrslugerðarþátta sem eru í keyrslu.
    - Þáttur líkanavörpunar fyrir þessa skilgreiningu er notaður til að draga gögn úr keyrðum sniðsþætti og síðan uppfæra forritstöflur.

    ![Skilgreining gagnalíkans rafrænnar skýrslugerðar fyrir innflutning gagna í runustillingu úr notendaviðmóti rafrænnar skýrslugerðar.](./media/er-configure-data-import-batch-configurations-2.png)

5. Opna skrána **1099import-data.xlsx** í Excel.

    ![Sýnishorn af Excel skrá með gögnum til innflutnings í runustillingu.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Virkja runugagnainnflutning fyrir rafræna skýrslugerð í notendaviðmótinu

1. Opna skal **Kerfisstjórnun** \> **Vinnusvæði** \> **Eiginleikastjórnun**.
2. Á vinnusvæðinu **Eiginleikastjórnun** skal velja eiginleikann **Keyra innflutning rafrænnar skýrslugerðar fyrir skjöl sem var hlaðið upp handvirkt í runu** og síðan velja **Virkja núna**.

## <a name="import-data-from-manually-selected-excel-files"></a>Flytja inn gögn úr handvirkt völdum Excel skrám

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar** skal velja skilgreining gagnalíkans **1099 Greiðslulíkan**.
3. Í flýtiflipanum **Skilgreiningarþættir** skal velja tengilinn **Fyrir 1099 handvirkan innflutning á færslum**.
4. Á síðunni **Líkanavörpun á gagnagjafa** er líkanavörpunin **Fyrir 1099 handvirkan innflutning á færslum** valin fyrirfram. Veljið **Keyra**.
5. Á flipanum **Færibreytur** skaltu velja **Fletta**. Finna og velja skrána **1099import-data.xlsx** og velja síðan **Í lagi**.
6. Í svæði **Slá inn auðkenni fylgiskjals**, skal slá inn **V-00001**.
7. Á flipanum **Keyra í bakgrunni**, skal stilla valkostinn **Runuvinnsla** á **Já**.

    Taktu eftir að reiturinn **Verklýsing** er stilltur á **Keyrsla líkanavörpunar „Fyrir 1099 handvirkan innflutning á færslum“, skilgreining „1099 Greiðslulíkan“**. Þetta gildi gefur til kynna að keyrsla valdrar líkanavörpunar verður tímasett sem ný runuvinnsla.

    ![Skilgreinir upplýsingar um gagnainnflutning í runustillingu í svarglugga rafrænna skýrslufæribreyta.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Veldu **Í lagi**. Skilaboð upplýsir þig um að ný runuvinnsla hafi verið tímasett.

    ![Skilaboð um nýja tímasetta runuvinnslu á síðu líkanavörpunar á gagnagjafa.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Farið yfir niðurstöður úr gagnainnflutningi á síðunni Runuvinnsla.

1. Farið í **Almennt** \> **Fyrirspurnir** \> **Runuvinnslur** \> **Mínar runuvinnslur**.
2. Á síðunni **Runuvinnsla** skal sía listann yfir runuvinnslur til að finna tímasetta runu og síðan velja hana.
3. Veldu hlekkinn fyrir **Vinnslukenni** til að yfirfara upplýsingar um starf.
4. Á flýtiflipanum **Runuverk** velurðu **Kladdi**.

    ![Kladdahnappur á runuvinnslusíðunni.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Yfirfara framkvæmdaupplýsingar

    ![Keyrsluskrá áætlaðrar runuvinnslu á síðunni Runuvinnsla.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Breyta færibreytum fyrir gagnainnflutning

Þegar runan er tímasett og hefur ekki enn verið keyrð er hægt að breyta færibreytum tímasetts gagnainnflutnings.

1. Farið í **Almennt** \> **Fyrirspurnir** \> **Runuvinnslur** \> **Mínar runuvinnslur**.
2. Á síðunni **Runuvinnsla** skal sía listann yfir runuvinnslur til að finna tímasetta runu og síðan velja hana.
3. Veljið **Breyta stöðu**.
4. Í svarglugganum **Velja nýja stöðu** er valið **Halda eftir** og síðan **Í lagi**.
5. Veldu tengilinn **Vinnslukenni** til að fá aðgang að starfsupplýsingum.
6. Á flýtiflipanum **Runuverk** velurðu **Færibreytur**.
7. Í svargluggann **Færibreytur rafrænnar skýrslugjafar** skal fylgja þessum skrefum:

    1. Veldu **Fletta** til að velja aðra skrá fyrir gagnainnflutning.
    2. Veldu **Slá inn auðkenni fylgiskjals** til að breyta fylgiskjalsnúmerinu fyrir innflutning lánardrottnafærslna.

        ![Breyting á færibreytum gagnainnflutnings fyrir tímasetta runuvinnslu í svarglugga fyrir rafrænar skýrslufæribreytur.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Veldu **Í lagi**.

8. Gakktu úr skugga um að runan sé enn valin og veldu svo **Breyta stöðu** aftur.
9. Í svarglugganum **Velja nýja stöðu** skal velja **Bíður** og svo velja **OK**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Fara yfir niðurstöður gagnainnflutnings á upprunasíðu rafrænnar skýrslugerðar

1. Farið í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Uppruni rafrænnar skýrslugerðar**.
2. Veldu færsluna **Fyrir innflutning lánardrottnafærslna (Excel)** sem var sjálfkrafa stofnuð við gagnainnflutninginn.

    ![Færsla fyrir skilgreiningu á Fyrir innflutning lánardrottnafærslna (Excel) á upprunasíðu rafrænnar skýrslugerðar.](./media/er-configure-data-import-batch-files-source-1.png)

3. Veljið **Skráarstöður fyrir uppruna**
4. Í flýtiflipunum **Skrár** og **Upprunakladdar fyrir innflutningssnið** skal fara yfir upplýsingar um innflutninginn.
5. Á flýtiflipanum **Skrár** skal velja færslu. Takið eftir því að innflutta skráin er tengd þessari færslu.

    ![Innflutt skrá hengd við færsluna á skráarstöðum fyrir upprunasíðuna.](./media/er-configure-data-import-batch-files-source-2.png)

6. Veldu **Viðhengi** til að fara yfir innfluttu skrána.

    ![Flutti inn skrá á síðu skjalayfirlits.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Til að halda þessum viðhengjum notar rammi rafrænnar skýrslugerðar skjalagerð sem er [stillt](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) fyrir núverandi fyrirtæki í reitnum **Annað** fyrir færibreytur rafrænnar skýrslugerðar.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Farið yfir niðurstöður gagnainnflutnings á síðu uppgjörs lánardrottins fyrir 1099s

1. Opnið **Viðskiptaskuldir** \> **Reglubundin verkefni** \> **Skattur 1099** \> **lánardrottins fyrir 1099**.
2. Í reitinn **Frá dagsetningu** skal slá inn **12/31/2017** (31. desember 2017).
3. Veljið **Handvirkar 1099-færslur**.

    ![Innfluttar lánardrottnafærslur á síðu 1099-skattfærslna.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
