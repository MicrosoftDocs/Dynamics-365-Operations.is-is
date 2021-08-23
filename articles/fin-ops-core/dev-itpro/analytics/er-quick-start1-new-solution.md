---
title: Hanna nýja lausn rafrænnar skýrslugerðar til að prenta sérsniðna skýrslu
description: Þetta efnisatriði útskýrir hvernig á að hanna lausn rafrænnar skýrslugerðar til að prenta sérsniðna skýrslu.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af610ae86e751ec4425f4c555cdf59c042fabcdb46e6a3a018b0d94a8926d92e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770069"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Hanna nýja lausn rafrænnar skýrslugerðar til að prenta sérsniðna skýrslu

[!include[banner](../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra, hönnuðar rafrænnar skýrslugerðar eða hagnýts ráðgjafa rafrænnar skýrslugerðar getur skilgreint færibreytur fyrir ramma rafrænnar skýrslugerðar, hannað nauðsynlegar skilgreiningar rafrænnar skýrslugerðar fyrir nýja lausn rafrænnar skýrslugerðar til að fá aðgang að gögnum tiltekins viðskiptaléns og útbúið sérsniðna skýrslu á Microsoft Office-sniði. Hægt er að ljúka skrefunum í **USMF** fyrirtækinu.

- [Skilgreina ramma rafrænnar skýrslugerðar](#ConfigureFramework)

    - [Skilgreina færibreytur Rafræn skýrslugerðar](#ConfigureParameters)
    - [Virkja skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider)

        - [Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar](#ReviewProvidersList)
        - [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#AddProvider)
        - [Virkja skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateAddedProvider)

- [Hanna gagnalíkan fyrir sérstakt lén](#DesignModel)

    - [Flytja inn nýja skilgreiningu gagnalíkans](#ImportDataModel)
    - [Stofna nýjan skilgreiningu gagnalíkans](#DesignDataModel)

        - [Gefa gagnalíkaninu heiti](#NameDataModel)
        - [Bæta við reitum gagnalíkans](#FieldsEntry)
        - [Ljúka hönnun gagnalíkansins](#CompleteDataModel)

- [Hanna líkanavörpun fyrir skilgreint gagnalíkan](#DesignMapping)

    - [Flytja inn nýja skilgreiningu líkanavörpunar](#ImportModelMapping)
    - [Stofna nýja skilgreiningu líkanavörpunar](#CreateModelMapping)

        - [Hanna nýjan þátt líkanavörpunar](#DesignMappingComponent)
        - [Bæta við gagnagjöfum til að fá aðgang að forritstöflum](#AddMmDataSource1)
        - [Bæta við gagnagjöfum til að fá aðgang að upptalningum forrits](#AddMmDataSource2)
        - [Bæta við merkjum rafrænnar skýrslugerðar til að búa til skýrslu á tilteknu tungumáli](#AddMmLabels)
        - [Bæta við gagnagjafa til að umbreyta niðurstöðunum við samanburð upptalningargilda og textagilda](#AddMmDataSource3)
        - [Tengja gagnagjafa við reiti gagnalíkans](#AddMmBindings1)
        - [Ljúka hönnun líkanavörpunar](#CompleteModelMapping)

- [Hanna sniðmát fyrir sérsniðna skýrslu](#DesignReportTemplate)
- [Setja upp snið](#DesignFormat)

    - [Flytja inn hannaða skilgreiningu sniðs](#FormatImport)
    - [Stofna nýja skilgreiningu á sniði](#FormatCreate)

        - [Flytja inn skýrslusniðmát](#ImportReportTemplate)
        - [Skilgreina snið](#ConfigureFormat)
        - [Skilgreina gagnatengslin fyrir titil skýrslu](#DefineFormatBindings)
        - [Fara yfir gagnagjafa líkans](#ReviewModelDataSource)
        - [Tengja sniðseiningar við reiti gagnagjafa](#BindFormatElements)

    - [Keyra hannað snið úr rafrænni skýrslugerð](#RunFormatFromER)

- [Stilla hannað snið](#TuneFormat)

    - [Laga snið til að breyta heiti á mynduðu skjali](#ModifyToChangeName)
    - [Laga snið til að breyta röð spurninga](#ModifyToOrder)
    - [Keyra breytt snið úr rafrænni skýrslugerð](#RunFormatFromER2)
    - [Ljúka hönnun sniðs](#CompleteFormat)

- [Þróa forritsgervinga til að kalla á hannaða skýrslu](#DevelopCustomCode)

    - [Breyta frumkóða](#ModifySourceCode)

        - [Bæta við gagnasamningsklasa](#DataContractClass)
        - [Bæta við smiðsklasa notendaviðmóts](#UIBuilderClass)
        - [Bæta við gagnagjafaklasa](#DataProviderClass)
        - [Bæta við merkjaskrá](#LabelsFile)
        - [Bæta við þjónustuklasa skýrslu](#ServiceClass)
        - [Bæta við stýriklasa skýrslu](#ControllerClass)
        - [Bæta við valmyndaratriði](#MenuItem)
        - [Bæta valmyndaratriði við valmynd](#Menu)
        - [Smíða Visual Studio-verk](#BuildVSProject)

    - [Keyra snið úr forritinu](#RunFormatFromApp)

- [Stilla hannaða lausn rafrænnar skýrslugerðar](#TuneSolution)

    - [Breyta líkanavörpun](#ModifyModelMapping)

        - [Bæta við gagnagjöfum til að fá aðgang að gagnasamningshlut](#AddDataSource1)
        - [Bæta við gagnagjafa til að fá aðgang að sniðsvörpunarfærslum rafrænnar skýrslugerðar](#AddDataSource2)
        - [Bæta við gagnagjafa til að fá aðgang að sniðsvörpunarfærslum rafrænnar skýrslugerðar](#AddDataSource3)
        - [Færið inn heiti á sniði rafrænnar skýrslugerðar sem er í gangi í gagnalíkaninu](#AddBinding)
        - [Ljúka hönnun líkanavörpunar](#CompleteModelMapping2)

    - [Breyta sniði](#ModifyFormat)

        - [Bæta við nýrri sniðseiningu](#AddFormatElement)
        - [Tengja viðbætta sniðseiningu](#BindAddedFormatElement)
        - [Ljúka sniðshönnun](#CompleteFormat2)

    - [Keyra snið úr forritinu](#RunFormatFromApp2)
    - [Keyra snið úr rafrænni skýrslugerð](#RunFormatFromER3)
    - [Skilgreina áfangastað sniðs fyrir forskoðun á skjá](#ConfigureDestination)
    - [Keyra snið úr forritinu til að forskoða það sem PDF-skjal](#RunFormatFromApp3)

- [Frekari upplýsingar](#References)

Í þessu dæmi er stofnuð ný lausn rafrænnar skýrslugerðar fyrir eininguna [Spurningalisti](../../../human-resources/hr-learning-questionnaires.md). Þessi nýja lausn rafrænnar skýrslugerðar gerir þér kleift að hanna skýrslu með því að nota Microsoft Excel-vinnublað sem sniðmát. Síðan er hægt að búa til skýrsluna **Spurningalisti** á Excel- eða PDF-sniði ásamt því að mynda fyrirliggjandi skýrslu SQL Server Reporting Services (SSRS). Einnig er hægt að breyta nýju skýrslunni seinna, ef um það er beðið. Ekki er þörf á neinni kóðun.

1. Til að keyra fyrirliggjandi skýrslu skal farið í **Spurningalisti** \> **Hanna** \> **Spurningalistaskýrsla**.

    ![Að velja valmyndaratriði spurningalistaskýrslunnar í spurningalistaeiningunni til að keyra fyrirliggjandi SSRS-skýrslu.](./media/er-quick-start1-application-menu-origin.png)

2. Í svarglugganum **Spurningalistaskýrsla** skal tilgreina valskilyrði. Notið síu þannig að skýrslan feli aðeins í sér spurningalistann **SBCCrsExam**.

    ![Tilgreina valskilyrði í svarglugga spurningalistaskýrslu.](./media/er-quick-start1-ssrs-report-dialog.png)

Eftirfarandi mynd sýnir útbúna útgáfu SSRS-skýrslunnar fyrir spurningalistann **SBCCrsExam**.

![Mynduð SSRS-skýrsla.](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að skilgreina lágmarkssafn af færibreytum rafrænnar skýrslugerðar áður en byrjað er að nota ramma rafrænnar skýrslugerðar til að hanna nýja lausn rafrænnar skýrslugerðar.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Í vinnusvæðinu **Rafræn skýrslugerð** velurðu **Rafrænar skýrslufæribreytur**.
3. Á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Almennt**, skal stilla valkostinn **Kveikja á hönnunarstillingu** á **Já**.
4. Í flipanum **Viðhengi** skal stilla eftirfarandi færibreytur:

    - Stillið reitinn **Skilgreiningar** á **Skrá** fyrir fyrirtækið **USMF**.
    - Stillið **Verksafn**, **Tímabundið**, **Grunnlína** og **Annað** reitina á **Skrá**.

Frekari upplýsingar um færibreytur rafrænnar skýrslugerðar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>Virkja skilgreiningarveitu rafrænnar skýrslugerðar

Allar skilgreiningar rafrænnar skýrslugerðar eru merktar í eigu skilgreiningarveitu rafrænnar skýrslugerðar. Þess vegna þarf að virkja skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð** áður en byrjað er að bæta við eða breyta einhverjum skilgreiningum rafrænnar skýrslugerðar.

> [!NOTE]
> Aðeins eigandi skilgreiningar rafrænnar skýrslugerðar getur breytt henni. Þess vegna, áður en hægt er að breyta skilgreiningu rafrænnar skýrslugerðar, verður að virkja viðeigandi skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Viðeigandi tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Skilgreiningarveitur** er hver færsla skilgreiningarveitu með einkvæmt heiti og vefslóð. Farið yfir efnið á þessari síðu. Ef færsla fyrir **Litware, Inc.** (`https://www.litware.com`) er þegar til skal sleppa næsta ferli, [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar

1. Á síðunni **Skilgreiningarveitur** skal velja **Ný**.
2. Í reitinn **Heiti** skal færa inn **Litware, Inc.**
3. Í reitinn **Veffang** skal færa inn `https://www.litware.com`.
4. Veljið **Vista**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>Virkja skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja skilgreiningarveituna **Litware, Inc**.
3. Veldu **Stilla sem virkt**.

Nánari upplýsingar um skilgreiningarveitur rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Hanna gagnalíkan fyrir sérstakt lén

Stofna þarf nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur [gagnalíkan](general-electronic-reporting.md#data-model-and-model-mapping-components)íhlut fyrir fyrirtækislénið **Spurningalisti**. Þetta gagnalíkan verður seinna notað sem gagnagjafi þegar hannað er snið rafrænnar skýrslugerðar til að búa til skýrsluna **Spurningalisti**.

Með því að ljúka skrefunum í hlutanum [Flytja inn nýja skilgreiningu gagnalíkans](#ImportDataModel) er hægt að flytja inn nauðsynlegt gagnalíkan úr uppgefinni XML-skrá. Að öðrum kosti er hægt að ljúka skrefunum í hlutanum [Stofna nýjan skilgreiningu gagnalíkans](#DesignDataModel) til að hanna þetta gagnalíkan frá grunni.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Flytja inn nýja skilgreiningu gagnalíkans

1. Sæktu skrána [Spurningalistar model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) og vistaðu hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.
5. Veljið **Fletta** og finnið síðan og veljið skrána **Spurningalistar model.version.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

Til að halda áfram skal sleppa næsta ferli, [Stofna nýjan skilgreiningu gagnalíkans](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Stofna nýjan skilgreiningu gagnalíkans

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
3. Veljið **Stofna skilgreiningu**.
4. Í fellistagluggann, í reitinn **Heiti**, skal færa inn **Líkan spurningalista**.
5. Veljið **Stofna skilgreiningu** til að stofna skilgreininguna.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Gefa gagnalíkaninu heiti

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan spurningalisti**.
2. Veljið **Hönnuður**.
3. Á síðunni **Hönnuður gagnalíkana**, í flýtiflipanum **Almennt**, í reitinn **Heiti**, skal færa inn <a name="DataModeName"></a>**Spurningalistar**.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Bæta við nýjum gagnalíkanareitum

1. Á síðunni **Hönnuður gagnalíkans** skal velja **Nýtt**.
2. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Veljið **Rót líkans** sem gerð nýja hnútsins.
    2. Í reitinn **Heiti** skal færa inn <a name="RootDefinitionName"></a>**Rót**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

    Þessi rótarlýsing verður notuð til að útvega gögn fyrir skýrsluna **Spurningalisti**. Eitt gagnalíkan getur haft margar lýsingar. Hver lýsing getur átt við um eitt snið rafrænnar skýrslugerðar til að finna gögn sem þarf til að mynda skýrsluna.

3. Veljið **Nýtt** aftur og síðan, í fellilistaglugganum til að bæta við gagnalíkanshnút, skal fylgja þessum skrefum:

    1. Veljið **Undireiningu virks hnúts** sem gerð nýja hnútsins.
    2. Í reitinn **Heiti** skal færa inn **CompanyName**.
    3. Í reitnum **Gerð vöru** velurðu **Strengur**.
    4. Veljið **Bæta við** til að bæta við nýja reitnum.

    Þessi reitur er nauðsynlegur til að flytja heiti núverandi fyrirtækis yfir í skýrslu rafrænnar skýrslugerðar sem notar þetta gagnalíkan sem gagnagjafa.

4. Veljið **Nýtt** aftur og síðan, í fellilistaglugganum til að bæta við gagnalíkanshnút, skal fylgja þessum skrefum:

    1. Veljið **Undireiningu virks hnúts** sem gerð nýja hnútsins.
    2. Í reitinn **Heiti** skal færa inn **Spurningalisti**.
    3. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
    4. Veljið **Bæta við** til að bæta við nýja reitnum.

    Þessi reitur verður notaður til að flytja lista af spurningalistum í skýrslu rafrænnar skýrslugerðar sem notar þetta gagnalíkan sem gagnagjafa.

5. Veljið hnútinn **Spurningalisti**.
6. Haldið áfram að bæta nauðsynlegum reitum við breytanlega gagnalíkanið með sama hætti þar til lokið er við eftirfarandi skipulag gagnalíkans.

    | Slóð á reit                                                    | Gagnagerð   | Tilnefndur reitur/skilað gildi |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Rót                                                          |             | Tilvísunarpunktur til að biðja um gögn spurningalista. |
    | Root\\CompanyName                                             | Strengur      | Heiti núverandi fyrirtækis. |
    | Root\\ExecutionContext                                        | Færsla      | Upplýsingar um keyrslusnið. |
    | Root\\ExecutionContext\\FormatName                            | Strengur      | Heiti sniðs rafrænnar skýrslugerðar sem verið er að keyra. |
    | Root\\Questionnaire                                           | Færslulisti | Listi yfir spurningalista |
    | Root\\Questionnaire\\Active                                   | Strengur      | Staða núverandi spurningalista. |
    | Root\\Questionnaire\\Code                                     | Strengur      | Kóði núverandi spurningalista. |
    | Root\\Questionnaire\\Description                              | Strengur      | Lýsing núverandi spurningalista. |
    | Root\\Questionnaire\\QuestionnaireType                        | Strengur      | Gerð núgildandi spurningalista. |
    | Root\\Questionnaire\\QuestionOrder                            | Strengur      | Númeraröð núgildandi spurningalista. |
    | Root\\Questionnaire\\ResultsGroup                             | Færsla      | Niðurstöðufæribreytur núverandi spurningalista. |
    | Root\\Questionnaire\\ResultsGroup\\Code                       | Strengur      | Auðkenniskóði núverandi niðurstöðuflokks. |
    | Root\\Questionnaire\\ResultsGroup\\Description                | Strengur      | Lýsing á núverandi niðurstöðuflokki. |
    | Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Rauntala        | Hámarksfjöldi punkta sem hægt var að vinna sér inn. |
    | Root\\Questionnaire\\Question                                 | Færslulisti | Listi yfir spurningar fyrir núverandi spurningalista. |
    | Root\\Questionnaire\\Question\\CollectionSequenceNumber       | Heiltala     | Raðnúmer núverandi samantekt af svörum. |
    | Root\\Questionnaire\\Question\\Id                             | Strengur      | Auðkenniskóði núverandi spurningar. |
    | Root\\Questionnaire\\Question\\MustBeCompleted                | Strengur      | Flagg sem gefur til kynna hvort svara þurfi núverandi spurningu. |
    | Root\\Questionnaire\\Question\\PrimaryQuestion                | Strengur      | Flagg sem segir til um hvort núverandi spurning er aðalspurning. |
    | Root\\Questionnaire\\Question\\SequenceNumber                 | Heiltala     | Raðnúmer núverandi spurningar. |
    | Root\\Questionnaire\\Question\\Text                           | Strengur      | Texti núverandi spurningar. |
    | Root\\Questionnaire\\Question\\Answer                         | Færslulisti | Svaralisti fyrir núverandi spurningu. |
    | Root\\Questionnaire\\Question\\Answer\\CorrectAnswer          | Strengur      | Flagg sem segir til um hvort núverandi svar er rétt. |
    | Root\\Questionnaire\\Question\\Answer\\Points                 | Rauntala        | Punktar sem eru unnir þegar gildandi svar er valið. |
    | Root\\Questionnaire\\Question\\Answer\\SequenceNumber         | Heiltala     | Raðnúmer núverandi svars. |
    | Root\\Questionnaire\\Question\\Answer\\Text                   | Strengur      | Texti núverandi svars. |

    Eftirfarandi mynd sýnir breytanlegt gagnalíkan sem er lokið á síðunni **Hönnuður gagnalíkans**.

    ![Skilgreint gagnalíkan í gagnalíkanahönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-model2.png)

7. Vista breytingarnar.
8. Lokið síðunni **Hönnuður gagnalíkans**.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Ljúka hönnun gagnalíkansins

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan spurningalisti**.
3. Í flýtiflipanum **Útgáfur** skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.
4. Veljið **Breyta stöðu** \> **Ljúka**.

Staða á útgáfu 1 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**. Ekki er lengur hægt að breyta útgáfu 1. Þessi útgáfa inniheldur skilgreinda gagnalíkanið og er hægt að nota sem grunninn fyrir aðrar skilgreiningar rafrænnar skýrslugerðar. Útgáfa 2 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**. Hægt er að breyta þessari útgáfu til að leiðrétta gagnalíkanið **Spurningalisti**.

![Útgáfur breytanlegrar skilgreiningar á skilgreiningarsíðunni.](./media/er-quick-start1-model-configuration.png)

Frekari upplýsingar um útgáfustjórnun fyrir skilgreiningar rafrænnar skýrslugerðar er að finna í [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Skilgreinda gagnalíkanið er óhlutdræg framsetning þín á fyrirtækisléninu **Spurningalisti** og inniheldur engin tengsl við gervinga sem eru sértækir fyrir Microsoft Dynamics 365 Finance.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Hanna líkanavörpun fyrir skilgreint gagnalíkan

Sem notandi í hönnunarhlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur íhlut [líkanavörpunar](general-electronic-reporting.md#data-model-and-model-mapping-components) fyrir gagnalíkanið **Spurningalisti**. Vegna þess að þessi íhlutur innleiðir skilgreint gagnalíkan fyrir Finance, á hann sérstaklega við um Finance. Skilgreina verður íhlut líkanavörpunar til að tilgreina hugbúnaðarhluti sem þarf að nota til að fylla út skilgreint gagnalíkan með forritsgögnum við keyrslu. Til að ljúka þessu verki þarf að gera sér grein fyrir upplýsingum innleiðingar fyrir gagnaskipulagið á fyrirtækisléninu **Spurningalisti** í Finance.

Með því að ljúka skrefunum í hlutanum [Flytja inn nýja skilgreiningu gagnalíkans](#ImportModelMapping) sem fylgja, er hægt að flytja inn nauðsynlega skilgreiningu líkanavörpunar úr uppgefinni XML-skrá. Að öðrum kosti er hægt að ljúka skrefunum í hlutanum [Stofna nýja skilgreiningu líkanavörpunar](#CreateModelMapping) til að hanna þessa líkanavörpun frá grunni.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Flytja inn nýja skilgreiningu líkanavörpunar

1. Sækið skrána [Spurningalistar mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) og vistið hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.
5. Veljið **Fletta** og finnið síðan og veljið skrána **Spurningalistar mapping.version.1.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

Til að halda áfram skal sleppa næsta ferli, [Stofna nýja skilgreiningu líkanavörpunar](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Stofna nýja skilgreiningu líkanavörpunar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan spurningalisti**.
3. Veljið **Stofna skilgreiningu**.
4. Í fellilistanum skaltu fylgja þessum skrefum:

    1. In the **New** field, select **Model Mapping based on data model Questionnaires**.
    2. Í reitinn **Heiti** skal færa inn **Vörpun spurningalista**.
    3. Í reitnum **Skilgreining gagnalíkans** skal velja **Rótar** skilgreininguna.
    4. Veljið **Stofna skilgreiningu** til að stofna skilgreininguna.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Hanna nýjan þátt líkanavörpunar

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun spurningalista**.
2. Veldu **Hönnuður** til að opna lista yfir varpanir.
3. Veljið vörpunina **Vörpun spurningalista** sem var sjálfkrafa bætt við fyrir **Rótar** skilgreininguna
4. Veljið **Hönnuður** til að hefja skilgreiningu á valdri vörpun.

Nýrri vörpun er sjálfkrafa bætt við fyrir **Rótar** skilgreininguna. Þessi vörpun er með stefnuna **Til líkans**. Þess vegna er hægt að nota þessa vörpun til að fylla út gagnalíkan með nauðsynlegum gögnum.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Bæta við gagnagjöfum til að fá aðgang að forritstöflum

Skilgreina þarf gagnagjafa til að fá aðgang að forritstöflum sem innihalda upplýsingar um spurningalista.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Töflufærslur**.
2. Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að töflunni KMCollection, þar sem sérhver færsla stendur fyrir stakan spurningalista:

    1. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    2. Í svarglugganum, í reitinn **Heiti**, skal færa inn **Spurningalisti**.
    3. Í reitinn **Tafla** skal færa inn **KMCollection**.
    4. Stillið valkostinn **Biðja um fyrirspurn** á **Já**. Þá er hægt að tilgreina valkosti [síunar](../../fin-ops/get-started/advanced-filtering-query-options.md) fyrir þessa töflu í svarglugga fyrirspurnar í kerfinu við keyrslu.
    5. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

3. Í rúðunni **Gerðir gagnagjafa** skal velja **Dynamics 365 for Operations\\Töflufærslur**.
4. Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að töflunni KMQuestion, þar sem sérhver færsla stendur fyrir staka spurningu í spurningalista:

    1. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    2. Í glugganum, í reitinn **Heiti**, skal slá inn **Spurning**.
    3. Í reitinn **Tafla** skal færa inn **KMQuestion**.
    4. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

5. Í rúðunni **Gerðir gagnagjafa** skal velja **Dynamics 365 for Operations\\Töflufærslur**.
6. Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að töflunni KMAnswer, þar sem sérhver færsla stendur fyrir eitt svar við spurningu í spurningalista:

    1. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    2. Í reitinn **Heiti** skal færa inn **Svar**.
    3. Í reitinn **Tafla** skal færa inn **KMAnswer**.
    4. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

7. Í rúðunni **Gerðir gagnagjafa** skal velja **Aðgerðir\\Reiknaður reitur**.
8. Bætið við nýjum reiknuðum reit sem verður notaður til að opna færslu í töflunni KMQuestionResultGroup úr öllum færslum í yfirtöflunni KMCollection:

    1. Í rúðunni **Gagnagjafar** skal velja **Spurningalisti**.
    2. Veljið **Bæta við**.
    3. Í glugganum, í reitinn **Heiti**, skal slá inn **\$ResultGroup**.
    4. Veljið **Breyta formúlu**.
    5. Í [Formúluritill rafrænnar skýrslugerðar](general-electronic-reporting-formula-designer.md), í reitinn **Formúla**, skal færa inn **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** til að nota [slóðina](er-formula-language.md#Paths) á tengslin „frá einu í margt“ milli taflanna KMCollection og KMQuestionResultGroup.
    6. Veljið **Vista** og lokið formúluritlinum.
    7. Veljið **Í lagi** til að bæta við nýja reiknaða reitnum.

9. Í rúðunni **Gerðir gagnagjafa** skal velja **Aðgerðir\\Reiknaður reitur**.
10. Bætið við nýjum reiknuðum reit sem verður notaður til að opna spurningafærslur í töflunni KMQuestion úr öllum færslum í yfirtöflunni KMCollectionQuestion:

    1. Í rúðunni **Gagnagjafar** skal velja **Spurningalisti**.
    2. Útvíkkið hnútinn **\<Tengsl** sem inniheldur tengslin „frá einu í margt“ á töflunni KMCollection.
    3. Veljið tengdu **KMCollectionQuestion** töfluna og veljið síðan **Bæta við**.
    4. Í glugganum, í reitinn **Heiti**, skal slá inn **\$Spurning**.
    5. Veljið **Breyta formúlu**.
    6. Í formúluritilinn, í reitinn **Formúla**, skal færa inn **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** til að skila viðeigandi spurningafærslum úr töflunni KMQuestion.
    7. Veljið **Vista** og lokið formúluritlinum.
    8. Veljið **Í lagi** til að bæta við nýja reiknaða reitnum.

11. Í rúðunni **Gerðir gagnagjafa** skal velja **Aðgerðir\\Reiknaður reitur**.
12. Bætið við nýjum reiknuðum reit sem verður notaður til að opna svarafærslur í töflunni KMAnswer úr öllum færslum í yfirtöflunni KMQuestion:

    1. Í rúðunni **Gagnagjafar** skal velja **Spurningalisti.\<Relations.KMCollectionQuestion.\$Question** og síðan velja **Bæta við**.
    2. Í glugganum, í reitinn **Heiti**, skal slá inn **\$Svar**.
    3. Veljið **Breyta formúlu**.
    4. Í formúluritilinn, í reitinn **Formúla**, skal slá inn **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** til að skila viðeigandi svarfærslum úr töflunni KMAnswer.
    5. Veljið **Vista** og lokið formúluritlinum.
    6. Veljið **Í lagi** til að bæta við nýja reiknaða reitnum.

13. Í rúðunni **Gerðir gagnagjafa** skal velja **Dynamics 365 for Operations\\Tafla**.
14. Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að aðferðum töflunnar CompanyInfo. Athugið að **find()** aðferðin í þessari töflu skilar færslu sem stendur fyrir fyrirtæki núverandi Finance-tilvik sem þessi vörpun er kölluð í samhengi við.

    1. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    2. Í glugganum, í reitinn **Heiti**, skal slá inn **CompanyInfo**.
    3. Í reitinn **Tafla** skal slá inn **CompanyInfo**.
    4. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Bæta við gagnagjöfum til að fá aðgang að upptalningum forrits

Skilgreina þarf gagnagjafa til að fá aðgang að upptalningum forrits og bera saman gildin við gildin í reitum af gerðinni **Upptalning** í forritstöflunum. Nota verður niðurstöðu samanburðarins til að fylla út viðeigandi reiti gagnalíkansins.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Upptalning**.
2. Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að gildum upptalningarinnar **EnumAppNoYes**:

    1. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    2. Í glugganum, í reitnum **Heiti**, skal slá inn **EnumAppNoYes**.
    3. Í reitinn **Upptalning** skal færa inn **NoYes**.
    4. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

3. Í rúðunni **Gerðir gagnagjafa** skal velja **Dynamics 365 for Operations\\Upptalning**.
4. Bætið við nýjum gagnagjafa sem verður notaður til að fá aðgang að gildum upptalningarinnar **KMCollectionQuestionMode**:

    1. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    2. Í glugganum, í reitnum **Heiti**, skal slá inn **EnumAppQuestionOrder**.
    3. Í reitinn **Upptalning** skal færa inn **KMCollectionQuestionMode**.
    4. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>Bæta við merkjum rafrænnar skýrslugerðar til að búa til skýrslu á tilteknu tungumáli

Hægt er að bæta við merkum rafrænnar skýrslugerðar til að skilgreina suma gagnagjafana þannig að þeir skili gildum sem eru háð tungumálinu sem er skilgreint í samhengi við kall líkanavörpunar.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnagjafar**, skal velja **Svar** og síðan velja **Breyta**.
2. Virkjið reitinn **Merki**.
3. Veldu **Þýða**.
4. Í svarglugganum **Textaþýðing** skal fylgja þessum skrefum:

    1. Í reitinn **Kenni merkis** skal færa inn **PositiveAnswer**.
    2. Í reitinn **Texti á sjálfgefnu tungumáli** skal færa inn **Já**.
    3. Veldu **Þýða**.
    4. Í reitinn **Kenni merkis** skal færa inn **NegativeAnswer**.
    5. Í reitinn **Texti á sjálfgefnu tungumáli** skal færa inn **No**.
    6. Veldu **Þýða**.

5. Lokið svarglugganum **Textaþýðing**.
6. Veldu **Hætta við**.

![Að bæta við merkjum rafrænnar skýrslugerðar fyrir breytanlega líkanavörpun.](./media/er-quick-start1-adding-labels.png)

Aðeins er búið að færa inn merki fyrir sjálfgefna tungumálið. Frekari upplýsingar um hvernig hægt er að þýða merki rafrænnar skýrslugerðar á önnur tungumál er að finna í [Hanna skýrslur á mörgum tungumálum](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Bæta við gagnagjafa til að umbreyta niðurstöðunum við samanburð upptalningargilda og textagilda

Fyrst að nauðsynlegt er að umbreyta niðurstöðum samanburðarins milli upptalningargilda og textagilda nokkrum sinnum fyrir mismunandi uppruna, er góð hugmynd að skilgreina þessi rök sem stakan gagnagjafa. Til að geta notað þennan gagnagjafa aftur þarf hinsvegar að skilgreina hann sem gagnagjafa með færibreytum. Frekari upplýsingar er að finna í [Styðja færibreytuköll á gagnagjöfum rafrænnar skýrslugerðar af gerðinni reiknaður reitur](er-calculated-field-type.md).

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Almennt\\Autt hólf**.
2. Bæta við nýju hólfi gagnagjafa:

    1. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    2. Í glugganum, í reitnum **Heiti**, skal slá inn **Hjálp**.
    3. Veljið **Í lagi** til að bæta við nýja hólfi gagnagjafans.

3. Í rúðunni **Gerðir gagnagjafa** skal velja **Aðgerðir\\Reiknaður reitur**.
4. Bæta við nýjum gagnagjafa:

    1. Í rúðunni **Gagnagjafar** skal velja **Hjálp**.
    2. Veljið **Bæta við**.
    3. Í glugganum, í reitinn **Heiti**, skal slá inn **NoYesEnumToString**.
    4. Veljið **Breyta formúlu**.
    5. Í formúluritlinum skal velja **Færibreytur**.
    6. Fylgið þessum skrefum til að tilgreina færibreytur fyrir skilgreinda segð:

        1. Veljið **Nýtt**.
        2. Í glugganum, í reitinn **Heiti**, skal slá inn **Frumbreyta**.
        3. Í reitinn **Gerð** skal velja gagnagerðina **Boolean**.
        4. Veljið **Í lagi**.

    7. Í reitinn **Formúla** skal slá inn **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** til að skila texta viðeigandi merkis rafrænnar skýrslugerðar, háð tungumálinu í samhengi við keyrsluna og gildi tiltekinnar færibreytu.
    8. Veljið **Vista** og lokið formúluritlinum.
    9. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

![Skilgreind líkanavörpun í hönnuði líkanavörpunar rafrænnar skýrslugerðar.](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Tengja gagnagjafa við reiti gagnalíkans

Nauðsynlegt er að tengja skilgreinda gagnagjafa við reiti gagnalíkansins til að tilgreina hvernig fyllt verðu út í gagnalíkanið með forritsgögnum við keyrslu.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnalíkan**, skal velja **CompanyName**.
2. Í rúðunni **Gagnagjafar** skal útvíkka **CompanyInfo** og síðan fylgja þessum skrefum:

    1. Útvíkkið hnútinn **CompanyInfo.find()** sem stendur fyrir aðferðina **find()** fyrir töfluna CompanyInfo.
    2. Veljið **CompanyInfo.find().Name**.
    3. Veljið **Tengja** til að fylla út heiti fyrirtækisins sem er í samhengi við skilgreinda líkanavörpun sem kallað er á við keyrslu.

3. Í rúðunni **Gagnalíkan** skal velja **Spurningalisti**.
4. Í rúðunni **Gagnagjafar** skal velja **Spurningalisti** og síðan velja **Tengja** til að fylla út í færslur spurningalista.
5. Í rúðunni **Gagnalíkan** skal útvíkka **Spurningalisti** og síðan fylgja þessum skrefum:

    1. Í rúðunni **Gagnalíkan** skal velja **Virkt**.
    2. Í rúðunni **Gagnalíkan** skal velja **Breyta**.
    3. Í reitinn **Formúla** skal færa inn **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** til að fylla út samanburð á upptalningargildum textaháðrar og tungumálaháðrar niðurstöðu.

6. Haldið áfram að tengja gagnagjafa við reiti gagnalíkans með sama hætti þar til eftirfarandi niðurstöðum er náð.

    | Slóð á reit                                              | Gagnagerð   | Aðgerð | Segð tengingar |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | Strengur      | Binda   | CompanyInfo.'find()'.Name |
    | Spurningalisti                                           | Færslulisti | Binda   | Spurningalisti |
    | Questionnaire\\Active                                   | Strengur      | Breyta   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Questionnaire\\Code                                     | Strengur      | Binda   | \@.kmCollectionId |
    | Questionnaire\\Description                              | Strengur      | Binda   | \@.Description |
    | Questionnaire\\QuestionnaireType                        | Strengur      | Binda   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Questionnaire\\QuestionOrder                            | Strengur      | Breyta   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, „Skilyrðisbundið“,<br>EnumAppQuestionOrder.Random, „Slembi (prósenta í spurningalista)“,<br>EnumAppQuestionOrder.RandomGroup, „Slembi (prósenta í niðurstöðuflokkum)“,<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | Questionnaire\\ResultsGroup                             | Færsla      |        | |
    | Questionnaire\\ResultsGroup\\Code                       | Strengur      | Binda   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Questionnaire\\ResultsGroup\\Description                | Strengur      | Binda   | \@.'\$ResultGroup'.description |
    | Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Rauntala        | Binda   | \@.'\$ResultGroup'.maxPoint |
    | Questionnaire\\Question                                 | Færslulisti | Binda   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Questionnaire\\Question\\CollectionSequenceNumber       | Heiltala     | Binda   | \@.answerCollectionSequenceNumber |
    | Questionnaire\\Question\\Id                             | Strengur      | Binda   | \@.kmQuestionId |
    | Questionnaire\\Question\\MustBeCompleted                | Strengur      | Breyta   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\PrimaryQuestion                | Strengur      | Binda   | \@.parentQuestionId |
    | Questionnaire\\Question\\SequenceNumber                 | Heiltala     | Binda   | \@.SequenceNumber |
    | Questionnaire\\Question\\Text                           | Strengur      | Binda   | \@.'\$Question'.text |
    | Questionnaire\\Question\\Answer                         | Færslulisti | Binda   | \@.'\$Question'.'\$Answer' |
    | Questionnaire\\Question\\Answer\\CorrectAnswer          | Strengur      | Breyta   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\Answer\\Points                 | Rauntala        | Binda   | \@.point |
    | Questionnaire\\Question\\Answer\\SequenceNumber         | Heiltala     | Binda   | \@.sequenceNumber |
    | Questionnaire\\Question\\Answer\\Text                   | Strengur      | Binda   | \@.text |

    Eftirfarandi mynd sýnir lokastöðu skilgreindrar líkanavörpunar á síðunni **Hönnuður líkanavörpunar**.

    ![Fullskilgreind líkanavörpun í hönnuði líkanavörpunar rafrænnar skýrslugerðar.](./media/er-quick-start1-mapping2.png)

7. Vista breytingarnar.
8. Lokið síðunni **Hönnuður líkanavörpunar**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Ljúka hönnun líkanavörpunar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun spurningalista**.
3. Í flýtiflipanum **Útgáfur** skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.
4. Veljið **Breyta stöðu** \> **Ljúka**.

Staða á útgáfu 1.1 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**. Ekki er lengur hægt að breyta útgáfu 1.1. Þessi útgáfa inniheldur skilgreindu líkanavörpunina og er hægt að nota sem grunninn fyrir aðrar skilgreiningar rafrænnar skýrslugerðar. Útgáfa 1.2 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**. Hægt er að breyta þessari útgáfu til að leiðrétta skilgreininguna **Vörpun spurningalista**.

![Útgáfur breytanlegra skilgreininga rafrænnar skýrslugerðar á skilgreiningarsíðunni.](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Skilgreinda líkanavörpunin er Finance-innleiðing á óhlutbundna gagnalíkaninu sem stendur fyrir fyrirtækislénið **Spurningalisti**.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Hanna sniðmát fyrir sérsniðna skýrslu

Rammi rafrænnar skýrslugerðar notar fyrirframskilgreind sniðmát til að búa til skýrslur á Microsoft Office-sniði (Excel-vinnubækur eða Word-skjöl). Á meðan nauðsynleg skýrsla er búin til, er sniðmát fyllt út með nauðsynlegum gögnum samkvæmt skilgreindu gagnaflæði. Þess vegna þarf fyrst að hanna sniðmát fyrir sérsniðnu skýrsluna. Þetta sniðmát verður að vera hannað sem Excel-vinnubók, skipulag þess sem stendur fyrir útlit sérsniðinnar skýrslu. Gefa þarf öllum Excel-atriðum heiti sem ætlunin er að fylla út í með nauðsynlegum gögnum.

1. Sækið skrána [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) og vistið hana á staðbundinni tölvu.
2. Opnið skrána í Excel og farið yfir skipulag vinnubókarinnar.

Eins og eftirfarandi mynd sýnir hefur sótt sniðmát verið hannað til að prenta tilgreinda spurningalista sem birta spurningar spurningalistans ásamt viðeigandi svörum.

![Excel-sniðmát til að prenta tilgreinda spurningalista.](./media/er-quick-start1-template-layout.png)

Excel-heitum hefur verið bætt við þetta sniðmát til að fylla út í upplýsingar um spurningalista. Hægt er að nota stjórnun heitis til að yfirfara Excel-heitin.

![Nota stjórnun heitis til að yfirfara Excel-heiti í uppgefnu Excel-sniðmáti.](./media/er-quick-start1-template-names.png)

Skýrslumerkjum hefur verið bætt við sem föstum texta á ensku. Hægt er að skipta út skýrslumerkjunum með nýjum Excel-heitum sem fylla út í merkin með tungumálaháðum texta með því að nota [merki](#AddMmLabels) fyrir snið rafrænnar skýrslugerðar, eins og gert var fyrir tungumálaháðar segðir í skilgreindu líkanavörpuninni. Í þessu tilviki verður að bæta við merkjum rafrænnar skýrslugerðar í breytanlegu sniði rafrænnar skýrslugerðar.

Eins og eftirfarandi mynd sýnir, hefur haus sérsniðinnar skýrslu verið tilgreindur til að gera síðuvíxl möguleg í Excel.

![Haus sérsniðinnar skýrslu í uppgefnu Excel-sniðmáti.](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Setja upp snið

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur [sniðs](general-electronic-reporting.md#FormatComponentOutbound) hluta. Skilgreina verður sniðshlutann til að tilgreina hvernig fyllt verður út í skýrslusniðmát með nauðsynlegum gögnum við keyrslu.

Með því að ljúka skrefunum í hlutanum [Flytja inn hannaða skilgreiningu sniðs](#FormatImport) er hægt að flytja inn nauðsynlegt snið úr uppgefinni XML-skrá. Að öðrum kosti er hægt að ljúka skrefunum í hlutanum [Stofna nýja skilgreiningu á sniði](#FormatCreate) til að hanna þetta snið frá grunni.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Flytja inn hannaða skilgreiningu sniðs

1. Sækið skrána [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) og vistið hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.
5. Veljið **Fletta** og finnið síðan og veljið skrána **Questionnaires format.version.1.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

Til að halda áfram skal sleppa næsta ferli, [Stofna nýja skilgreiningu sniðs](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Stofna nýja skilgreiningu á sniði
 
1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan spurningalisti**.
3. Veljið **Stofna skilgreiningu**.
4. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í reitnum **Nýtt** skal velja **Snið byggir á spurningalistum gagnalíkans**.
    2. Í reitinn **Heiti** skal færa inn **Skýrsla spurningalista**.
    3. Í reitnum **Útgáfa gagnalíkans** skal velja **1**.

        > [!NOTE]
        > - Ef valin er sérstök útgáfa af grunngagnalíkaninu verður skipulag samsvarandi útgáfu gagnalíkansins kynnt þér sem skipulag gagnagjafans **Líkan** á sniðinu sem stofnað er.
        > - Hægt er að skilja þennan reit eftir auðan. Í því tilfelli verður skipulag útgáfunnar **Drög** fyrir gagnalíkanið kynnt þér sem skipulag gagnagjafans **Líkan** á sniðinu sem stofnað er. Síðan er hægt að leiðrétta líkanið og sjá svo leiðréttingarnar strax í sniðinu. Þessi nálgun gæti bætt skilvirkni á hönnun á lausnum rafrænnar skýrslugerðar þegar gagnalíkanið, líkanavörpunin og sniðið er skilgreint á sama tíma.
        > - Ef valin er sérstök útgáfa af grunngagnalíkaninu er hægt að skipta yfir í að nota útgáfuna **Drög** seinna, þegar hafist er handa við að breyta sniðinu.

    4. Í reitnum **Skilgreining gagnalíkans** skal velja **Rótar** skilgreininguna.

5. Veljið **Stofna skilgreiningu** til að stofna skilgreininguna.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Flytja inn skýrslusniðmát

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Skýrsla spurningalista**.
2. Veljið **Hönnuður** til að hefja skilgreiningu á sérsniðnu sniði.
3. Á síðunni **Sniðshönnuður**, í aðgerðarúðunni, skal velja **Flytja inn** \> **Flytja inn úr Excel**.
4. Í svarglugganum skal fylgja þessum skrefum:

    1. Veljið **Bæta við sniðmáti**.
    2. Finnið og veljið staðbundið vistuðu skrána **Questionnaires report template.xslx** og veljið síðan **Opna**.
    3. Veljið **Í lagi** til að flytja inn sniðmátið.

    ![Flytja inn skýrslusniðmát.](./media/er-quick-start1-template-import.png)

Sniðseiningin **Excel\\File** er sjálfkrafa bætt við breytanlega sniðið sem rótareining. Þar að auki er annaðhvort sniðseiningin **Excel\\Range** eða sniðseiningin **Excel\\Cell** sjálfkrafa bætt við fyrir hvert viðurkennt Excel-heiti á innfluttu sniðmáti. Sniðið **Excel\\Header** sem er með földuðu eininguna **Strengur** er sjálfkrafa bætt við til að endurspegla hausstillingar á innfluttu sniðmáti.

![Sniðsskipulag sem inniheldur sjálfkrafa viðbættum einingum í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Skilgreina snið

1. Á síðunni **Sniðshönnuður**, í sniðstrénu, skal velja rótareininguna **Excel**.
2. Í flipanum **Snið** hægra megin á síðunni, í reitnum **Heiti**, skal færa inn <a name="AddFormatRootElement"></a>**Skýrsla**.
3. Í reitnum **Tungumálastillingar** skal velja **Kjörstilling notanda** til að keyra skýrsluna á kjörtungumáli notanda.
4. Í reitnum **Kjörstillingar menningar** skal velja **Kjörstilling notanda** til að keyra skýrsluna samkvæmt kjörmenningu notanda.

    Frekari upplýsingar um hvernig á að tilgreina samhengi tungumáls og menningar fyrir ferli rafrænnar skýrslugerðar er að finna í [Hanna skýrslur á mörgum tungumálum](er-design-multilingual-reports.md).

    ![Stillingar tungumáls og menningar fyrir hannaða skýrslu í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-template-format-structure1.png)

5. Í sniðstrénu skal útvíkka rótarhnútinn og velja ´siðan **ResultsGroup**.
6. Í flipanum **Snið**, í reitnum **Stefna eftirlíkingar**, skal velja **Engin eftirlíking** því að þú býst ekki við því að fá marga niðurstöðuflokka fyrir einn spurningalista.

    ![Skilgreining á stefnu eftirlíkingar fyrir sniðseininguna Svið í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-template-format-structure2.png)

7. Veldu **Vista**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Skilgreina gagnatengslin fyrir titil skýrslu

Tilgreina verður gagnatengsl fyrir sniðseiningu sem er notuð til að fylla út titil á myndaðri skýrslu.

1. Á síðunni **Sniðshönnuður**, í flipanum **Vörpun** hægra megin, skal velja eininguna **Report\\ReportTitle**.
2. Veljið **Breyta formúlu**.
3. Í formúluritlinum skal velja **Þýða**.
4. Í svarglugganum **Textaþýðing** skal fylgja þessum skrefum:

    1. Í reitinn **Kenni merkis** skal færa inn **ReportTitle**.
    2. Í reitinn **Texti á sjálfgefnu tungumáli** skal færa inn **Spurningalistaskýrsla**.
    3. Veljið **Þýða** og veljið síðan **Vista**.
    4. Veljið **Þýða** til að loka svarglugganum **Textaþýðing**.

5. Lokið formúluritlinum.

    ![Skilgreining tengingar til að fylla út í titilinn á myndaðri skýrslu.](./media/er-quick-start1-add-report-title-label.png)

Hægt er að nota þessa tækni til að gera öll önnur merki núverandi sniðmáts tungumálaháð. Frekar upplýsingar um hvernig hægt er að þýða viðbætt merki á einni skilgreiningu rafrænnar skýrslugerðar yfir á öll studd tungumál er að finna í [Hanna skýrslur á mörgum tungumálum](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Fara yfir gagnagjafa líkans

1. Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, skal velja gagnagjafann <a name="ModelDSName"></a>**líkan** sem stendur fyrir grunngagnalíkan þessa sniðs rafrænnar skýrslugerðar.
2. Veljið **Breyta**.
3. Yfirfara upplýsingarnar í svarglugganum **Eiginleikar gagnagjafa**. Þessi gagnagjafi stendur fyrir útgáfu 1 af gagnalíkanshlutanum **Spurningalistar** sem er að finna í **Líkan spurningalista** fyrir skilgreiningu rafrænnar skýrslugerðar.

![Eiginleikar gagnagjafa líkansins í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Tengja sniðseiningar við reiti gagnagjafa

Til að tilgreina hvernig sniðmát er fyllt út við keyrslu verður að tengja hverja sniðseiningu sem tengist viðeigandi Excel-heiti við stakan reit í gagnagjafa þessa sniðs.

1. Á síðunni **Sniðshönnuður**, í sniðstrénu, skal velja sniðseininguna **Report\\CompanyName**.
2. Í flipanum **Vörpun** skal velja gagnagjafareitinn **model.CompanyName** af gerðinni **Strengur**.
3. Veljið **Tengja** til að færa inn fyrirtækisheiti í sniðmáti.
4. Í sniðstrénu er valinn einingin **Report\\Questionnaire**.
5. Í flipanum **Vörpun** skal velja gagnagjafareitinn **model.Questionnaire** af gerðinni **Færslulisti**.
6. Veldu **Binda**.
7. Veljið **Sýna upplýsingar** til að fá nánari upplýsingar um sniðseiningar.

    Sviðssniðseiningin **Spurningalisti** er skilgreind sem endurtekin lóðrétt. Þegar hún er tengd við gagnagjafa af gerðinni **Færslulisti** er viðeigandi sviðið **Spurningalisti** af Excel-sniðmátinu endurtekið fyrir allar skrár tengda gagnagjafans.
 
    ![Að tengja sviðssniðseiningu spurningalistans við viðeigandi gagnagjafa færslulista í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-bindings1.png)

    Þar sem sviðið **Spurningalisti** í Excel-sniðmátinu er skilgreint milli línu 5 og 14, eru þessar líknur endurteknar fyrir hvern uppgefinn spurningalista.

    ![Línur í Excel-sniðmátinu sem verða endurteknar í myndaðri skýrslu fyrir hverja færslu í gagnagjafa færslulistans.](./media/er-quick-start1-template-questionnaire-range.png)

8. Skilgreinið svipaðar tengingar fyrir eftirstandandi sniðseiningar, eins og lýst er í eftirfarandi töflu.

    > [!NOTE]
    > Í þessari töflu er í upplýsingunum í dálknum „Slóð gagnagjafa“ gert ráð fyrir að kveikt sé á [tengdri slóð](relative-path-data-bindings-er-models-format.md) eiginleika rafrænnar skýrslugerðar.

    | Slóð sniðseiningar                                      | Slóð gagnagjafa |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Questionnaire                                     | **model.Questionnaire** |
    | Excel\\Questionnaire\\Active                             | **\@.Active**, þar sem **\@** er **model.Questionnaire** |
    | Excel\\Questionnaire\\Code                               | **\@.Code** |
    | Excel\\Questionnaire\\Description                        | **\@.Description** |
    | Excel\\Questionnaire\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Questionnaire\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Questionnaire\\ResultsGroup\\Code\_               | **\@.ResultsGroup.Code** |
    | Excel\\Questionnaire\\ResultsGroup\\Description\_        | **\@.ResultsGroup.Description** |
    | Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Questionnaire\\Question                           | **\@.Question** |
    | Excel\\Questionnaire\\Question\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, þar sem **\@** er **model.Questionnaire.Question** |
    | Excel\\Questionnaire\\Question\\Id                       | **\@.Id** |
    | Excel\\Questionnaire\\Question\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Questionnaire\\Question\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Questionnaire\\Question\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Questionnaire\\Question\\Text                     | **\@.Text** |
    | Excel\\Questionnaire\\Question\\Answer                   | **\@.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer    | **\@.CorrectAnswer**, þar sem **\@** er **model.Questionnaire.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\Points           | **\@.Points** |
    | Excel\\Questionnaire\\Question\\Answer\\Text             | **\@.Text** |

9. Þegar þessu er lokið skal velja **Vista**.

Eftirfarandi mynd sýnir lokastöðu skilgreindra gagnatengsla á síðunni **Sniðshönnuður**.

![Skilgreind gagnatengsl í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Allt safn tilgreindra gagnagjafa og tengsla stendur fyrir sniðsvörpunaríhlut fyrir skilgreinda sniðið. Kallað er á þessa sniðsvörpun þegar skilgreint snið fyrir skýrslumyndun er keyrt.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Keyra hannað snið úr rafrænni skýrslugerð

Nú er hægt að keyra hannað snið í prófunartilgangi af síðunni **Skilgreiningar**.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreining**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Spurningalistaskýrsla**.
3. Veljið **Hönnuður** fyrir sniðsútgáfuna sem er með stöðuna **Drög**.
4. Á síðunni **Sniðshönnuður** skal velja **Keyra**.
5. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.
6. Veljið **Í lagi** til að staðfesta síunarvalkostinn.
7. Veljið **Í lagi** til að keyra skýrsla.
8. Farið yfir myndaða skýrslu.

Mynduð skýrsla er [sjálfgefið](electronic-reporting-destinations.md#default-behavior) afhent sem Excel-skrá sem hægt er að sækja. Eftirfarandi myndir sýna tvær síður af myndaðri skýrslu á Excel-sniði.

![Dæmi um myndaða skýrslu á Excel-sniði, síða 1.](./media/er-quick-start1-report1a.png)

![Dæmi um myndaða skýrslu á Excel-sniði, síða 2.](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Stilla hannað snið

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Laga snið til að breyta heiti á mynduðu skjali

Sjálfgefið er að myndað skjal sé nefnt með því að nota samnefni núverandi notanda. Með því að breyta sniðinu er hægt að breyta þessari hegðun þannig að mynduðu skjali sé gefið heiti sem byggir á sérstilltum rökum. Til dæmis er hægt að byggja heiti myndaðs skjals á núverandi dagsetningu og tíma lotunnar og á titli skýrslunnar.

1. Á síðunni **Sniðshönnuður** skal velja rótaratriðið **Skýrsla**.
2. Í flipanum **Vörpun** skal velja **Breyta skráarheiti**.
3. Í reitinn **Formúla** skal færa inn **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.
4. Veljið **Vista** og lokið formúluritlinum.
5. Veljið **Vista**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Laga snið til að breyta röð spurninga

Spurningunum er ekki rétt raðað í myndaðri skýrslu. Hægt er að breyta röðinni með því að breyta sniðinu.

1. Á síðunni **Sniðshönnuður** skal velja rótaratriðið **Skýrsla**.
2. Í flipanum **Vörpun**, í sniðstrénu, skal útvíkka **Report\\Questionnaire\\Question**.

    ![Sniðseining spurningar af sviðsgerðinni í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-bindings3.png)

3. Í flipanum **Vörpun** skal velja **model.Questionnaire**.
4. Veljið **Bæta við** \> **Functions\\Calculated field** og því næst, í reitinn **Heiti**, skal færa inn **OrderedQuestions**.
5. Veljið **Breyta formúlu**.
6. Í formúluritilinn, í reitinn **Formúla**, skal færa inn **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** til að raða lista yfir spurningar í núgildandi spurningalista eftir númeraröðinni.
7. Veljið **Vista** og lokið formúluritlinum.
8. Veljið **Í lagi** til að ljúka færslu á nýjum reiknuðum reit.
9. Í flipanum **Vörpun** skal velja **model.Questionnaire.OrderedQuestions**.
10. Í sniðstrénu skal velja **Excel\\Questionnaire\\Question**.
11. Veljið **Tengja** og staðfestið síðan að núverandi slóðinni **model.Questionnaire.Questions** sé skipt út fyrir nýju slóðina **model.Questionnaire.OrderedQuestions** í öllum tengslum faldaðra eininga.
12. Veljið **Vista**.

![Tengja sniðseiningu spurningar við skilgreinda gagnagjafann OrderedQuestions í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Keyra breytt snið úr rafrænni skýrslugerð

Nú er hægt að keyra breytt snið í prófunartilgangi í ramma rafrænnar skýrslugerðar.

1. Á síðunni **Sniðshönnuður** skal velja **Keyra**.
2. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.
3. Veljið **Í lagi** til að staðfesta síunarvalkostinn.
4. Veljið **Í lagi** til að keyra skýrsla.
5. Farið yfir myndaða skýrslu.

Eftirfarandi mynd sýnir myndaða skýrslu á Excel-sniði þar sem spurningunum er rétt raðað.

![Mynduð skýrsla á Excel-sniði sem er með rétt röðuðum spurningum.](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Ljúka sniðshönnun

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Spurningalistaskýrsla**.
3. Í flýtiflipanum **Útgáfur** skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.
4. Veljið **Breyta stöðu** \> **Ljúka**.

Staða á útgáfu 1.1 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**. Ekki er lengur hægt að breyta útgáfu 1.1. Þessi útgáfa inniheldur skilgreinda sniðið og er hægt að nota til að prenta sérsniðnu skýrsluna. Útgáfa 1.2 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**. Hægt er að breyta þessari útgáfu til að leiðrétta snið skýrslunnar **Spurningalisti**.

![Breytanleg skilgreining rafrænnar skýrslugerðar á skilgreiningarsíðunni.](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Skilgreinda sniðið er hönnunin þín á skýrslunni **Spurningalisti** og hefur engin tengsl við sérstaka Finance-gervinga.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Þróa forritsgervinga til að kalla á hannaða skýrslu

Sem notandi í hlutverki kerfisstjóra þarf að þróa ný rök þannig að hægt sé að kalla á skilgreint snið rafrænnar skýrslugerðar úr notendaviðmóti forritsins til að mynda sérsniðnu skýrsluna. Sem stendur býður rafræn skýrslugerð er ekki upp á neina möguleika á því að skilgreina þessa gerð af rökum. Þess vegna er einhver hönnunarvinna nauðsynleg. 

Til að þróa nýju rökin þarf að setja upp grannfræði sem styður samfellda smíði. Nánari upplýsingar er að finna [Setja upp grannfræði sem styður samfellda smíði og sjálfvirkni prófunar](../perf-test/continuous-build-test-automation.md). Þú verður einnig að hafa aðgang að þróunarumhverfi fyrir þessa grannfræði. Frekari upplýsingar um tiltækt API rafrænnar skýrslugerðar er að finna í [API fyrir ramma rafrænnar skýrslugerðar](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Breyta frumkóða

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Bæta við gagnasamningsklasa

Bætið nýja klasanum **QuestionnairesErReportContract** við Microsoft Visual Studio-verkið og skrifið kóða sem tilgreinir gagnasamninginn sem á að nota til að keyra skilgreint snið rafrænnar skýrslugerðar.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>Bæta við smiðsklasa notendaviðmóts

Bætið nýja klasanum **QuestionnairesErReportUIBuilder** við Visual Studio-verkið og skrifið kóða til að mynda svarglugga við keyrslutíma sem verður notaður til að fletta upp á auðkenni sniðsvörpunar fyrir snið rafrænnar skýrslugerðar sem þarf að keyra. Uppgefinn kóði flettir aðeins upp á sniðum rafrænnar skýrslugerðar sem innihalda gagnagjafa af gerðinni **Gagnalíkan** sem vísar til gagnalíkansins **[Spurningalistar](#DataModeName)** með því að nota skilgreininguna **[Rót](#RootDefinitionName)**.

> [!NOTE]
> Einnig er hægt að nota samþættingarstaði rafrænnar skýrslugerðar til að sía snið rafrænnar skýrslugerðar. Frekari upplýsingar er að finna í [API til að sýna uppflettingu sniðsvörpunar](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Bæta við gagnaveituklasa

Bætið nýja klasanum **QuestionnairesErReportDP** við Visual Studio-verkið og skrifið kóða sem tilgreinir gagnaveituna sem á að nota til að keyra skilgreint snið rafrænnar skýrslugerðar. Uppgefinn kóði inniheldur aðeins gagnasamninginn fyrir þessa gagnaveitu.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Bæta við merkjaskrá

Bætið nýju **QuestionnairesErReportLabels\_en-US** merkjaskránum við Visual Studio-verkið og tilgreinið eftirfarandi töflur fyrir ný tilföng notendaviðmóts:

- Merkið **\@QuestionnairesReport** fyrir nýtt valmyndaratriði sem inniheldur eftirfarandi texta á bandarískri ensku (en-US): **Skýrsla spurningalista (knúin af rafrænni skýrslugerð)**
- Merkið **\@QuestionnairesReportBatchJobDescription** fyrir titil runuvinnslu ef valið snið rafrænnar skýrslugerðar er áætlað fyrir keyrslu sem runuvinnsla

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Bæta við þjónustuklasa skýrslu

Bætið nýja klasanum **QuestionnairesErReportService** við Visual Studio-verkið og skrifið kóða sem kallar á snið rafrænnar skýrslugerðar, finnur það eftir auðkenni sniðsvörpunar og gefur upp gagnasamning sem færibreytu.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Þegar þarf að nota snið rafrænnar skýrslugerðar sem keyrir forritsgögn þarf að skilgreina gagnagjafa af gerðinni **Gagnalíkan** í sniðsvörpuninni. Þessi gagnagjafi vísar til ákveðins hluta tiltekins gagnalíkans með því að nota eina rótarskilgreiningu. Þegar snið rafrænnar skýrslugerðar er keyrt, kallar það á þennan gagnagjafa til að opna viðeigandi líkanavörpun rafrænnar skýrslugerðar sem er skilgreind fyrir uppgefið líkan og rótarskilgreiningu.

Allar upplýsingar sem kunna að vera undirbúnar í frumkóðanum og verslun sem hluti af gagnasamningnum er hægt að flytja yfir í snið rafrænnar skýrslugerðar sem er í gangi með því að nota líkanavörpun rafrænnar skýrslugerðar af þessari gerð. Í líkanavörpun rafrænnar skýrslugerðar þarf að skilgreina gagnagjafa af gerðinni **Hlutur** sem vísar til klasans **[QuestionnairesErReportContract](#DataContractClass)**. Til að auðkenna líkanavörpun þarf að tilgreina gagnagjafa sem kallar á þessa líkanavörpun. Í uppgefnum kóða er þessi gagnagjafi tilgreindur af fastanum **ERModelDataSourceName** sem er með gildið fyrir **[líkan](#ModelDSName)**. Til að gera grein fyrir því hvaða gagnagjafi er notaður til að birta gagnasamninginn í líkanavörpuninni þarf að tilgreina heiti gagnagjafa. Í uppgefnum kóða er þetta heiti tilgreint af fastanum **ParametersDataSourceName** sem er með gildið <a name="DataContractDSName"></a>**RunTimeParameters**.

> [!NOTE]
> Í nýju umhverfi gæti þurft að uppfæra lýsigögn rafrænnar skýrslugerðar þannig að þessi gerð af klasa sé tiltæk í hönnuði líkanavörpunar í rafrænni skýrslugerð. Frekari upplýsingar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Bæta við stýriklasa skýrslu

Bætið nýja klasanum **QuestionnairesErReportController** við Visual Studio-verkið og skrifið kóða sem keyrir snið rafrænnar skýrslugerðar í annaðhvort samstilltri stillingu eða runustillingu, eftir þörfum, í svarglugganum sem er smíðaður samkvæmt rökunum fyrir uppgefinn klasa **QuestionnairesErReportUIBuilder**.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Bæta við valmyndaratriði

Bætið nýja valmyndaratriðinu **QuestionnairesErReport** við Visual Studio-verkið. Í eiginleikanum **Hlutur**, vísar þetta valmyndaratriði til klasans **QuestionnairesErReportController** og hann er notaður til að tilgreina heimild notanda til að velja og keyra snið rafrænnar skýrslugerðar. Í eiginleikanum **Merki**, vísar þetta valmyndaratriði til merkisins **\@QuestionnairesReport** sem var búið til hér á undan, þannig að réttur texti er sýndur í notendaviðmóti forritsins.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Bæta valmyndaratriði við valmynd

Bæta núverandi valmyndinni **Þekkingarstjórnun** við Visual Studio-verkið. Bæta þarf nýju **QuestionnairesErReport** atriði af gerðinni **Úttak** við þessa valmynd. Þetta atriði verður að vísa til valmyndaratriðisins **QuestionnairesErReport** sem er lýst í fyrri hlutanum.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Smíða Visual Studio-verk

Smíðið verkið til að búa til nýtt valmyndaratriði sem verður í boði fyrir notendur.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Keyra snið úr forritinu

1. Farið í **Spurningalisti** \> **Hönnun** \> **Skýrsla spurningalista (knúin af rafrænni skýrslugerð)**.

    ![Að velja valmyndaratriði spurningalistaskýrslunnar (knúin af rafrænni skýrslugerð) í spurningalistaeiningunni til að keyra skilgreint snið rafrænnar skýrslugerðar.](./media/er-quick-start1-application-menu-modified.png)

2. Í svarglugganum, í reitnum **Sniðsvörpun**, skal velja **Spurningalistaskýrsla**.
3. Veljið **Í lagi**.
4. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.
5. Veljið **Í lagi** til að staðfesta síunarvalkostinn.
6. Veljið **Í lagi** til að keyra skýrsla.

    ![Að tilgreina valskilyrðin í svarglugga rafrænnar skýrslugerðar.](./media/er-quick-start1-report-run-dialog-page.png)

7. Farið yfir myndaða skýrslu.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Stilla hannaða lausn rafrænnar skýrslugerðar

Hægt er að breyta skilgreindri lausn rafrænnar skýrslugerðar þannig að hún noti klasa gagnaveitunnar sem var þróuð til að fá aðgang að upplýsingum um snið rafrænnar skýrslugerðar sem er í gangi, og þannig að hún færi inn heiti á þessu snið rafrænnar skýrslugerðar í myndaðri skýrslu.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Breyta líkanavörpun

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Bæta við gagnagjöfum til að fá aðgang að gagnasamningshlut

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Vörpun spurningalista**.
3. Veljið **Hönnuður** til að opna síðuna **Líkanavörpun á gagnagjafa**.
4. Veljið **Hönnuður** til að opna valda vörpun í hönnuði líkanavörpunar.
5. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Hlutur**.
6. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
7. Í svarglugganum, í reitinn **Heiti**, skal færa inn **[RunTimeParameters](#DataContractDSName)**, eins og það er skilgreint í frumkóða klasans **QuestionnairesErReportService**.
8. Í reitinn **Klasi** skal færa inn **[QuestionnairesErReportContract](#DataContractClass)**, sem var kóðaður hér áður.
9. Veljið **Í lagi**.
10. Útvíkkið **RunTimeParameters**.

Viðbættur gagnagjafi veitir upplýsingar um færslukenni á sniðsvörpun rafrænnar skýrslugerðar sem er í gangi.

![Viðbættur gagnagjafi í hönnuði sniðsvörpunar rafrænnar skýrslugerðar.](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Bæta við gagnagjafa til að fá aðgang að sniðsvörpunarfærslum rafrænnar skýrslugerðar

Haldið áfram að breyta valdri líkanavörpun með því að bæta við gagnagjafa til að fá aðgang að vörpunarfærslum á sniði rafrænnar skýrslugerðar.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Töflufærslur**.
2. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
3. Í glugganum, í reitinn **Heiti**, skal slá inn **ER1**.
4. Í reitinn **Tafla** skal slá inn **ERFormatMappingTable**.
5. Veljið **Í lagi**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Bæta við gagnagjafa til að fá aðgang að sniðsvörpunarfærslum rafrænnar skýrslugerðar

Haldið áfram að breyta valdri líkanavörpun með því að bæta við gagnagjafa til að fá aðgang að vörpunarfærslum á sniði rafrænnar skýrslugerðar sem er í gangi.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Functions\\Calculated field**.
2. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
3. Í glugganum, í reitinn **Heiti**, skal slá inn **ER2**.
4. Veljið **Breyta formúlu**.
5. Í formúluritilinn, í reitinn **Formúla**, skal færa inn **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.
6. Veljið **Vista** og lokið formúluritlinum.
7. Veljið **Í lagi**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Færið inn heiti á sniði rafrænnar skýrslugerðar sem er í gangi í gagnalíkaninu

Haldið áfram að breyta valdri líkanavörpun þannig að heiti á snið rafrænnar skýrslugerðar sem er í gangi sé fært inn í gagnalíkanið.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnalíkan**, skal útvíkka **ExecutionContext** og síðan velja **ExecutionContext\\FormatName**.
2. Í rúðunni **Gagnalíkan** skal velja **Breyta** til að skilgreina gagnatengsl fyrir valinn reit gagnalíkansins.
3. Í formúluritilinn, í reitinn **Formúla**, skal færa inn **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.
4. Veljið **Vista** og lokið formúluritlinum.

Þar sem reiturinn **FormatName** var notaður, sýnir skilgreind líkanavörpun nú heitið á snið rafrænnar skýrslugerðar sem kallar á þessa líkanavörpun í keyrslunni.

![Að tengja reit gagnalíkansins við aðferð viðbætta gagnagjafans í hönnuði sniðsvörpunar rafrænnar skýrslugerðar.](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Ljúka hönnun líkanavörpunar

1. Á síðunni **Hönnuður líkanavörpunar** skal velja **Vista**.
2. Lokið síðunni.
3. Lokið síðunni Líkanavarpanir.
4. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal ganga úr skugga um skilgreiningin **Vörpun spurningalista** sé enn valin. Því næst, í flýtiflipanum **Útgáfur**, skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.
5. Veljið **Breyta stöðu** \> **Ljúka**.

Staða á útgáfu 1.2 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**. Ekki er lengur hægt að breyta útgáfu 1.2. Þessi útgáfa inniheldur skilgreindu líkanavörpunina og er hægt að nota sem grunninn fyrir aðrar skilgreiningar rafrænnar skýrslugerðar. Útgáfa 1.3 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**. Hægt er að breyta þessari útgáfu til að leiðrétta líkanavörpunina **Spurningalisti**.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Breyta sniði

Hægt er að breyta skilgreindu sniði rafrænnar skýrslugerðar þannig að heiti þess sé sýnt í síðufæti skýrslu sem er mynduð þegar snið rafrænnar skýrslugerðar er keyrt.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Bæta við nýrri sniðseiningu

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Spurningalistaskýrsla**.
3. Veljið **Hönnuður**.
4. Á síðunni **Sniðshönnuður** skal velja rótaratriðið **Skýrsla**.
5. Veljið **Bæta við** til að bæta nýrri faldaðri sniðseiningu fyrir valið rótaratriðið **Skýrsla**.
6. Veljið **Excel\\Footer**.
7. Í reitinn **Heiti** skal færa inn **Síðufótur**.
8. Veljið **Skýrsla/Síðufótur** og því næst veljið **Bæta við**.
9. Veljið **Text\\String**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Tengja viðbætta sniðseiningu

1. Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, í sniðstrénu, fyrir virku eininguna **Footer\\String**, skal velja **Breyta formúlu**.
2. Í formúluritilinn, í reitinn **Formúla**, skal færa inn **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.
3. Veljið **Vista** og lokið formúluritlinum.
4. Veljið **Vista**.

Skilgreinda sniðinu hefur nú verið breytt þannig að heiti þess verður fært inn í síðufótinn á myndaðri skýrslu með því að nota eininguna **Footer\\String**.

![Að bæta sniðseiningu síðufóts við skilgreint snið í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Ljúka sniðshönnun

1. Lokaðu síðunni **Sniðshönnuður**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal ganga úr skugga um skilgreiningin **Skýrsla spurningalista** sé enn valin. Því næst, í flýtiflipanum **Útgáfur**, skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.
3. Veljið **Breyta stöðu** \> **Ljúka**.

Staða á útgáfu 1.2 fyrir þessa skilgreiningu er breytt úr **Drög** í **Lokið**. Ekki er lengur hægt að breyta útgáfu 1.2. Þessi útgáfa inniheldur skilgreinda sniðið og er hægt að nota sem grunninn fyrir aðrar skilgreiningar rafrænnar skýrslugerðar. Útgáfa 1.3 af þessari skilgreiningu er stofnuð og er með stöðuna **Drög**. Hægt er að breyta þessari útgáfu til að leiðrétta skýrsluna **Spurningalisti**.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Keyra snið úr forritinu

1. Farið í **Spurningalisti** \> **Hönnun** \> **Skýrsla spurningalista (knúin af rafrænni skýrslugerð)**.
2. Í svarglugganum, í reitnum **Sniðsvörpun**, skal velja **Spurningalistaskýrsla**.
3. Veljið **Í lagi**.
4. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.
5. Veljið **Í lagi** til að staðfesta síunarvalkostinn.
6. Veljið **Í lagi** til að keyra skýrsla.
7. Farið yfir myndaða skýrslu á Excel-sniði.

Takið eftir að síðufótur myndaðrar skýrslu inniheldur heiti á sniði rafrænnar skýrslugerðar sem var notað til að mynda hana.

![Mynduð skýrsla á Excel-sniði.](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Keyra snið úr rafrænni skýrslugerð

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal útvíkka **Líkan spurningalista** og velja síðan **Spurningalistaskýrsla**.
3. Í aðgerðarúðunni skal velja **Keyra**.
4. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.
5. Veljið **Í lagi** til að staðfesta síunarvalkostinn.
6. Veljið **Í lagi** til að keyra skýrsla.
7. Farið yfir myndaða skýrslu á Excel-sniði.

Takið eftir því að síðufótur myndaðrar skýrslu inniheldur ekki heitið á sniði rafrænnar skýrslugerðar sem var notað til að mynda hana, því að gagnasamningshluturinn var ekki færður yfir í líkanavörpunina sem er í gangi þegar snið rafrænnar skýrslugerðar sem var keyrt úr rafrænni skýrslugerð kallaði á hana.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Skilgreina áfangastað sniðs fyrir forskoðun á skjá

1. Fara á **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.
2. Á síðunni **Viðtökustaður rafrænnar skýrslugerðar** skal bæta við færslu viðtökustaðar fyrir skilgreint snið **Skýrsla spurningalista** fyrir rafræna skýrslugerð.
3. Í flýtiflipanum **Viðtökustaður skráar** skal setja upp **Skjá** [Viðtökustaðar](er-destination-type-screen.md) fyrir sniðsíhlutinn **Skýrsla** sem hefur verið [bætt við](#AddFormatRootElement) sem rótareiningu skilgreindrar **Skýrslu spurningalista** fyrir snið rafrænnar skýrslugerðar.
4. Í flýtiflipanum **Umbreytingarstillingar PDF-skjals** skal skilgreina viðtökustaðinn til að umbreyta skýrslu í [PDF-snið](electronic-reporting-destinations.md#OutputConversionToPDF) sem notar síðuuppsetninguna **Langsnið**.

![Að skilgreina sérsniðinn viðtökustað skjás fyrir snið rafrænnar skýrslugerðar á viðtökusíðu rafrænnar skýrslugerðar.](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Keyra snið úr forritinu til að forskoða það sem PDF-skjal

1. Farið í **Spurningalisti** \> **Hönnun** \> **Skýrsla spurningalista (knúin af rafrænni skýrslugerð)**.
2. Í svarglugganum, í reitnum **Sniðsvörpun**, skal velja **Spurningalistaskýrsla**.
3. Veljið **Í lagi**.
4. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar**, í flýtiflipanum **Færslur til að taka með**, skal skilgreina síunarvalkostinn þannig að aðeins spurningalistinn **SBCCrsExam** er hafður með.
5. Veljið **Í lagi** til að staðfesta síunarvalkostinn.

    Takið eftir að í flýtiflipanum **Viðtökustaðir** er reiturinn **Úttak** stilltur á **Skjár**. Ef ætlunin er að breyta skilgreindum viðtökustað skal velja **Breyta**.

    ![Svargluggi keyrslu fyrir skýrslu rafrænnar skýrslugerðar þar sem hægt er að breyta skilgreindum viðtökustað.](./media/er-quick-start1-run-settings.png)

6. Veljið **Í lagi** til að keyra skýrsla.
7. Farið yfir myndaða skýrslu á PDF-sniði.

    ![Forskoðun myndaðrar skýrslu á PDF-sniði.](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)
- [Hanna skýrslur á mörgum tungumálum](er-design-multilingual-reports.md)
- [API fyrir ramma rafrænnar skýrslugerðar](er-apis-app73.md)
- [CASE-aðgerð](er-functions-logical-case.md)
- [CONCATENAT-aðgerð](er-functions-text-concatenate.md)
- [DATETIMEFORMAT-aðgerð](er-functions-datetime-datetimeformat.md)
- [FILTER-aðgerð](er-functions-list-filter.md)
- [FIRSTORNULL-aðgerð](er-functions-list-firstornull.md)
- [FORMAT-aðgerð](er-functions-text-format.md)
- [IF-aðgerð](er-functions-logical-if.md)
- [ORDERBY-aðgerð](er-functions-list-orderby.md)
- [SESSIONNOW-aðgerð](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
