---
title: Flytja inn gögn úr skrám sem voru valdar handvirkt í runustillingu
description: Þessi grein útskýrir hvernig á að flytja inn gögn úr handvirkt völdum skrám í lotuham.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288229"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Flytja inn gögn úr skrám sem voru valdar handvirkt í runustillingu

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Til að nota [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) ramma til að flytja inn gögn úr handvirkt völdum skrám á heimleið í lotuham, stilla ER [sniði](er-overview-components.md#format-component) sem styður innflutninginn. Þá keyra a [módelkortlagningu](er-overview-components.md#model-mapping-component) af **Á áfangastað** gerð sem notar það snið sem gagnagjafa. Til að flytja inn gögn skaltu fletta að skránni sem þú vilt flytja inn og velja hana handvirkt. 

Nýja ER-getan sem styður gagnainnflutning í lotuham gerir kleift að stilla þetta ferli sem eftirlitslaust. Þú getur notað ER stillingar til að framkvæma gagnainnflutning með því að tímasetja nýtt runuverk frá ER notendaviðmótinu (UI).

Þessi grein útskýrir hvernig á að ljúka gagnainnflutningi úr handvirkt valinni skrá í lotuham. Dæmin nota lánardrottnafærslur sem viðskiptagögn. Hægt er að ljúka skrefum þessara dæma í **USMF** fyrirtæki. Ekki er þörf á neinni kóðun.

## <a name="prerequisites"></a>Forkröfur

Til að klára dæmin í þessari grein verður þú að hafa eftirfarandi aðgang:

- Eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- ER snið og líkanstillingar fyrir 1099 greiðslur

### <a name="create-the-required-er-configurations"></a>Búðu til nauðsynlegar ER stillingar

Til að búa til nauðsynlegar ER-stillingar og fá aðrar forsendur skaltu fylgja einu af þessum skrefum:

- Spila **ER flytja inn gögn úr Microsoft Excel skrá** verkefnaleiðbeiningar, sem eru hluti af **7.5.4.3 Fá/Þróa upplýsingatækniþjónustu/lausn íhlutir (10677)** viðskiptaferli. Þessar verkefnaleiðbeiningar útskýra fyrir þér ferlið við að hanna og nota ER stillingar sem flytja inn færslur söluaðila gagnvirkt frá Microsoft Excel skrár. Nánari upplýsingar er að finna í [Þátta skjöl á innleið á Excel-sniði](parse-incoming-documents-excel.md).
- Ljúktu við dæmin í [Stilla gagnainnflutning frá SharePoint](er-configure-data-import-sharepoint.md). Þessi dæmi útskýra fyrir þér ferlið við að hanna og nota ER stillingar sem flytja inn færslur söluaðila gagnvirkt úr Excel skrám sem eru geymdar í SharePoint möppu.

### <a name="download-the-required-er-configurations"></a>Sæktu nauðsynlegar ER stillingar

1. Sæktu eftirfarandi ER stillingar og vistaðu þær á staðnum.

    | Lýsing á efni | Skrá |
    |---------------------|------|
    | **1099 Greiðslulíkan** Uppsetning ER gagnalíkans | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Til að flytja inn viðskipti söluaðila (Excel)** ER snið stillingar | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Nota [Hlaða úr XML skrá](er-defer-sequence-element.md#import-the-sample-er-configurations) ER valkostur til að flytja inn niðurhalaðar ER stillingar í tilvikið þitt af Dynamics 365 Finance í eftirfarandi röð:

    1. Skilgreining á gagnalíkani í ER
    2. ER Sníða skilgreiningu

### <a name="download-the-required-excel-files"></a>Sæktu nauðsynlegar Excel skrár

- Sæktu eftirfarandi sýnishornsgagnasett og vistaðu það á staðnum.

    | Lýsing á efni | Skrá |
    |---------------------|------|
    | Á heimleið **1099import-data.xlsx** skrá sem inniheldur sýnishorn til innflutnings | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Farið yfir forsendur

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á **Stillingar** síðu, skoðaðu tilbúna ER lausn fyrir gagnainnflutning í lotuham.
3. Skoðaðu **Til að flytja inn viðskipti söluaðila (Excel)** sniðstillingar.

    - Sniðshluti þessarar uppsetningar er hannaður til að flokka Excel-skrá á heimleið.
    - Líkanskortlagningarhluti þessarar uppsetningar er notaður til að fylla út grunngagnalíkanið með því að nota gögn úr þáttuðu Excel skránni.

    ![ER snið stillingar til að flytja inn gögn í lotuham frá ER UI.](./media/er-configure-data-import-batch-configurations-1.png)

4. Skoðaðu **1099 Greiðslulíkan** uppsetningu gagnalíkana.

    - Líkanhluti þessarar uppsetningar táknar uppbyggingu gagnalíkans sem er notað til að senda gögn á milli hlaupandi ER íhluta.
    - Líkanskortlagningarhluti þessarar uppsetningar er notaður til að draga gögn úr keyrðu sniðhlutanum og uppfæra síðan forritatöflur.

    ![Uppsetning ER gagnalíkans til að flytja inn gögn í lotuham frá ER UI.](./media/er-configure-data-import-batch-configurations-2.png)

5. Opnaðu **1099import-data.xlsx** skrá í Excel.

    ![Sýnishorn af Excel skrá með gögnum til innflutnings í lotuham.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Virkjaðu runugagnainnflutning fyrir ER frá notendaviðmótinu

1. Opna skal **Kerfisstjórnun** \> **Vinnusvæði** \> **Eiginleikastjórnun**.
2. Í **Eiginleikastjórnun** vinnusvæði, veldu **Keyra ER innflutning handvirkt hlaðið upp skjölum í lotu** eiginleiki og veldu síðan **Virkja núna**.

## <a name="import-data-from-manually-selected-excel-files"></a>Flytja inn gögn úr handvirkt völdum Excel skrám

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á **Stillingar** síðu, veldu **1099 Greiðslulíkan** uppsetningu gagnalíkana.
3. Á **Stillingaríhlutir** flýtiflipann, veldu **Fyrir 1099 handvirkar færslur innflutningur** hlekkur.
4. Á **Líkan til kortlagningar gagnagjafa** síðu, the **Fyrir 1099 handvirkar færslur innflutningur** líkanakortlagning er forvalin. Veljið **Keyra**.
5. Á **Færibreytur** flipa, veldu **Skoðaðu**. Finndu og veldu **1099import-data.xlsx** skrá og veldu síðan **Allt í lagi**.
6. Í **Sláðu inn auðkenni skírteinis** reit, slá inn **V-00001**.
7. Á **Hlaupa í bakgrunni** flipann, stilltu **Lotuvinnsla** valmöguleika til **Já**.

    Taktu eftir því að **Verkefnalýsing** reiturinn er stilltur á **Keyrsla líkanavörpunar 'Fyrir 1099 handvirkar færslur innflutning', stillingar '1099 greiðslulíkan'**. Þetta gildi gefur til kynna að framkvæmd valinna líkanavörpunar verði tímasett sem nýtt runuverk.

    ![Tilgreina upplýsingar um innflutning gagna í lotuham í færibreytum rafrænna skýrslu.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Veldu **Í lagi**. Skilaboð láta þig vita að nýtt runuverk hafi verið tímasett.

    ![Skilaboð um nýtt áætlað runuverk á kortlagningarsíðunni Líkan til gagnagjafar.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Skoðaðu niðurstöður gagnainnflutnings á runuvinnusíðunni

1. Farið í **Almennt** \> **Fyrirspurnir** \> **Runuvinnslur** \> **Mínar runuvinnslur**.
2. Á **Lotuvinna** síðu, síaðu listann yfir runuvinnu til að finna áætlaða lotu og veldu hana síðan.
3. Veldu **Starfskenni** hlekkur til að skoða upplýsingar um starfið.
4. Á **Lotuverkefni** Flýtiflipi, veldu **Log**.

    ![Log hnappur á runuverkssíðunni.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Farðu yfir framkvæmdaupplýsingarnar.

    ![Framkvæmdaskrá fyrir áætlaða runuvinnu á síðunni Runuverk.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Breyttu innflutningsbreytum gagna

Eftir að runan þín hefur verið áætluð og á meðan hún hefur ekki enn verið keyrð geturðu breytt færibreytum áætlaðs gagnainnflutnings.

1. Farið í **Almennt** \> **Fyrirspurnir** \> **Runuvinnslur** \> **Mínar runuvinnslur**.
2. Á **Lotuvinna** síðu, síaðu listann yfir runuvinnu til að finna áætlaða lotu og veldu hana síðan.
3. Veljið **Breyta stöðu**.
4. Í **Veldu nýja stöðu** valmynd, veldu **Halda eftir**, og veldu síðan **Allt í lagi**.
5. Veldu **Starfskenni** hlekkur til að fá aðgang að upplýsingum um starfið.
6. Á **Lotuverkefni** Flýtiflipi, veldu **Færibreytur**.
7. Í **Rafræn skýrslufæribreytur** valmynd, fylgdu þessum skrefum:

    1. Veldu **Skoðaðu** til að velja aðra skrá fyrir gagnainnflutning.
    2. Veldu **Sláðu inn auðkenni skírteinis** til að breyta fylgiskjalsnúmeri fyrir innflutning lánardrottinsfærslur.

        ![Að breyta færibreytum gagnainnflutnings fyrir áætlaða runuvinnu í svarglugganum Færibreytur rafrænna skýrslu.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Veldu **Í lagi**.

8. Gakktu úr skugga um að lotan sé enn valin og veldu síðan **Breyta stöðu** aftur.
9. Í **Veldu nýja stöðu** valmynd, veldu **Bíður**, og veldu síðan **Allt í lagi**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Skoðaðu niðurstöður gagnainnflutnings á ER upprunasíðunni

1. Fara til **Stjórn stofnunarinnar** \> **Rafræn skýrslugerð** \> **Rafræn skýrslugjafi**.
2. Veldu **Til að flytja inn viðskipti söluaðila (Excel)** skrá sem var sjálfkrafa búin til við innflutning gagna.

    ![Skrá fyrir stillinguna Til að flytja inn færslur lánardrottna (Excel) á síðunni Uppruni rafrænnar skýrslugerðar.](./media/er-configure-data-import-batch-files-source-1.png)

3. Veldu **Skráarríki fyrir heimildirnar**.
4. Á **Skrár** og **Heimildaskrár fyrir innflutningssniðið** Flýtiflipar, skoðaðu innflutningsupplýsingarnar.
5. Á **Skrár** Flýtiflipi, veldu færsluna. Taktu eftir að innflutta skráin er tengd þessari skrá.

    ![Innflutt skrá sem fylgir skránni á síðunni Skráarástand fyrir heimildasíðuna.](./media/er-configure-data-import-batch-files-source-2.png)

6. Veldu **Viðhengi** til að skoða innfluttu skrána.

    ![Innflutt skrá á síðunni Skjalaskoðun.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Til að halda þessum viðhengjum notar ER ramma skjalagerð sem er [sett](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) fyrir núverandi fyrirtæki í **Aðrir** reit ER færibreytanna.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Skoðaðu niðurstöður gagnainnflutnings á síðunni Uppgjör lánardrottins fyrir 1099s

1. Fara til **Viðskiptaskuldir** \> **Reglubundin verkefni** \> **Skattur 1099** \> **Seljendauppgjör fyrir 1099s**.
2. Í **Frá dags** reit, slá inn **31.12.2017** (31. desember 2017).
3. Veldu **Handvirk 1099 viðskipti**.

    ![Innfluttar lánardrottnafærslur á Tax 1099 færslur síðunni.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
