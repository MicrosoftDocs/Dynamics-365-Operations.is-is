---
title: Notaðu JOIN gagnaheimildir í ER-líkanavörpun til að fá gögn úr mörgum töflum forrita
description: Þessi grein útskýrir hvernig hægt er að nota gagnagjafa af JOIN-gerð í rafrænni skýrslugerð (ER).
author: kfend
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 3f03e69dbce7c9039f22dbb8f3afa06f16d9c080
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285152"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Notaðu JOIN gagnaheimildir til að fá gögn úr mörgum forritatöflum í líkanavörpun í rafrænni skýrslugerð (ER)

[!include[banner](../includes/banner.md)]

Við stillingu á líkanavörpun eða sniðmáta rafrænnar skýrslugerðar (ER) er hægt að [bæta við](#review) áskilins gagnagjafa af gerðinni **Join**. Á hönnunartíma er gagnagjafi **Join** stilltur sem mengi nokkurra gagnagjafa, sem hver og einn skila lista yfir færslur. Fyrir hverja gagnagjafa nema þann fyrsta þarftu að skilgreina nauðsynleg skilyrði til að sameina skrár yfir núverandi og fyrri gagnaheimildir. Gagnagjafi af gerðinni **Join** [skilar](#executeERformat) einum sameinuðum lista yfir skrár sem innihalda reiti úr skrám með ívöfðum gagnagjöfum á keyrslutíma.

Eftirfarandi samtengingar eru studdar eins og stendur:

- Ytri (vinstri) samtenging:
    - Sameinaðu allar skrár fyrsta (vinstra) gagnagjafans og síðan allar samsvarandi í samræmi við stilltar skilyrðaskrár í síðari (hægri) gagnagjafanum.
- Innri (hægri) samtenging:
    - Sameinaðu aðeins skrár fyrsta (vinstra) gagnagjafans og aðeins skrár í síðari (hægri) gagnagjafanum sem eru samsvarandi í samræmi við stillt skilyrði.

Í stillta gagnagjafanum **Join**, þegar allir gagnagjafar eru af gerðinni **Töflufærslur**, getur framkvæmd á Join-gagnagjafanum verið [framkvæmd á gagnagrunnsstigi](#analyze) að nota eina SQL-skipun. Þetta uppgjör dregur úr fjölda gagnagrunnskalla, sem bætir afköst líkansvarpana. Annars er framkvæmd á **Join** gagnagjafa framkvæmd í minni.

> [!NOTE]
> Notkun á virkninni **VALUEIN** í ER-segðum sem tilgreina skilyrði fyrir sameiningu á skrám í gagnagjöfum af gerðinni Join er ekki enn studd. Farið á síðuna [Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md) til að fá frekari upplýsingar um þessa virkni.

Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka dæminu í þessari grein.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Dæmi: Notaðu JOIN gagnagjafa í ER-líkanavörpun

Eftirfarandi skref útskýra hvernig kerfisstjóri eða þróunaraðili rafrænnar skýrslugerðar getur stillt líkanavörpun rafrænnar skýrslugerðar (ER) til að sækja gögn úr mörgum forritatöflum í einu með því að nota gagnagjafa af gerðinni **Join** til að bæta afköst gagnaaðgangs. Hægt er að framkvæma þessi skref fyrir eitthvert fyrirtæki Dynamics 365 Finance eða Regulatory Configuration Services (RCS).

### <a name="prerequisites"></a>Forkröfur

Til að ljúka dæmunum í þessari grein verður þú að hafa aðgang að einu af eftirtöldu eftir því hvaða þjónusta er notuð til að ljúka þessum skrefum:

**Aðgangur að Finance fyrir eitt af eftirfarandi hlutverkum:**

- Þróunaraðili rafrænnar skýrslulausnar
- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

**Aðgangi RCS fyrir eitt af eftirfarandi hlutverkum:**

- Þróunaraðili rafrænnar skýrslulausnar
- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Einnig verður fyrst að ljúka við skrefin í ferlinu [Stofna skilgreiningarveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Fyrirfram þarf einnig að sækja og vista eftirfarandi sýnishorn af skilgreiningarskrá rafrænnar skýrslugerðar:

| **Lýsing á efni**  | **Skrárnafn**   |
|--------------------------|-----------------|
| Sýnishorn af stillingaskránni **ER-gagnalíkan** sem er notuð sem gagnagjafi fyrir dæmin.| [Model to learn JOIN data sources.version.1.1.xml](https://download.microsoft.com/download/5/c/1/5c1d8a57-6ebd-425b-bc5d-c71dde92c6af/ModeltolearnJOINdatasources.version.1.xml) |
| Sýnishorn af stillingaskránni **ER-líkanavörpun** sem innleiðir ER-gagnalíkanið fyrir dæmin. | [Vörpun til að læra JOIN gagnagjafa.útgáfu.1.1.xml](https://download.microsoft.com/download/9/2/f/92f339ca-41fc-4f5e-b458-6983c957d3dd/MappingtolearnJOINdatasources.version.1.1.xml)|
| Sýnishorn af stillingaskrá **ER-sniðs**. Þessi skrá lýsir gögnum til að fylla út ER-sniðsíhlut fyrir dæmin. | [Sniðmát til að læra JOIN gagnagjafa.útgáfu.1.1.xml](https://download.microsoft.com/download/f/f/8/ff8f1b48-14d0-4c73-9145-bcdf8b5265bc/FormattolearnJOINdatasources.version.1.1.xml) |

### <a name="activate-a-configurations-provider"></a>Kveikja á stillingaveitu

1. Fáðu aðgang að annaðhvort Finance eða RCS í fyrstu lotu vafrans.
2. Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.
3. Á síðunni **Skilgreiningar staðfærslu**, í hlutanum **Skilgreiningaveitur**, skal ganga úr skugga um að skilgreiningaveitan fyrir sýnifyrirtækið [Litware, Inc.](http://www.litware.com) sé skráð og merkt sem **Virkt**. Ef þú sérð skilgreiningarveituna ekki skaltu fylgja skrefunum í ferlinu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Vinnusvæði rafrænnar skýrslugerðar.](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>Flytja inn sýnishorn af ER-stillingaskrám

1. Veldu **Skilgreiningar skýrslugerðar**.
2. Flytja inn stillingarskrá ER-gagnalíkansins.
    1. Veldu **Gengi**.
    2. Veldu **Hlaða úr XML-skrá**.
    3. Veldu **Fletta** til að finna skjalið **Model to learn JOIN data sources.version.1.1.xml**.
    4. Veljið **Í lagi**.
3. Flytja inn skilgreiningarskrá líkanavörpunar rafrænnar skýrslugerðar.
    1. Veldu **Gengi**.
    2. Veldu **Hlaða úr XML-skrá**.
    3. Veldu **Fletta** til að finna skjalið **Mapping to learn JOIN data sources.version.1.1.xml**.
    4. Veljið **Í lagi**.
4. Flytja inn skilgreiningarskrá ER-sniðs.
    1. Veldu **Gengi**.
    2. Veldu **Hlaða úr XML-skrá**.
    3. Veldu **Fletta** til að finna skjalið **Format to learn JOIN data sources.version.1.1.xml**.
    4. Veljið **Í lagi**.
5. Í skilgreiningatrénu skaltu stækka liðinn **Model to learn JOIN data sources** ásamt öðrum líkanaliðum (þegar þeir eru í boði).
6. Fylgstu með lista yfir ER stillingar í trénu ásamt upplýsingum um útgáfu á flýtiflipanum **Útgáfur** - þeir verða notaðir sem gagnagjafi fyrir skýrslusýnishornið.

    ![Síðan Skilgreiningar rafrænnar skýrslugerðar.](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Kveiktu á rakningarvalkostum framkvæmdar

1. Veldu **CONFIGURATIONS**.
2. Veldu **Færibreytur notanda**.
3. Stilltu rakningarfæribreytur framkvæmdar eins og sýnt er á skjámyndinni hér að neðan.

    ![Síðan Færibreytur notanda rafrænnar skýrslugerðar.](./media/GER-JoinDS-Parameters.PNG)

    Þegar kveikt er á þessum færibreytum verður framkvæmdarmerki myndað fyrir hverja framkvæmd á innfluttri skrá ER-sniðs. Með því að nota upplýsingar um myndaða framkvæmdarakningu er hægt að greina framkvæmt sniðs rafrænnar skýrslugerðar og hluta líkanavörpunar rafrænnar skýrslugerðar. Farðu á síðuna [Rekja framkvæmd á ER-sniði til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md) til að fá frekari upplýsingar um eiginleika ER-framkvæmdamerkis.

### <a name="review-er-model-mapping-part-1"></a>Skoðaðu vörpun ER-líkans (hluti 1)

Yfirfara stillingar á hlut líkanavörpunar rafrænnar skýrslugerðar. Íhluturinn er stilltur til að fá aðgang að upplýsingum um útgáfur af ER-stillingum, upplýsingum um stillingar og stillingarveitendur án þess að nota heimildir um gerð **Join**.

1. Veldu skilgrieninguna **Mapping to learn JOIN data sources**.
2. Veldu **Hönnuður** til að opna lista yfir varpanir.
3. Veldu **Hönnuður** til að fara yfir upplýsingar um varpanir.
4. Veljið **Sýna upplýsingar**.
5. Í skilgreiningatrénu stækkarðu gagnalíkansliðina **Set1** og **Set1.Details**:

    1. Bindandi **Upplýsingar: Skráalisti = Útgáfur** gefur til kynna að liðurinn **Set1.Details** vera bundinn við gagnagjafann **Útgáfur** sem skilar gögnum um töfluna **ERSolutionVersionTable**. Hver skrá í þessari töflu táknar eina útgáfu af ER-stillingum. Efni þessarar töflu er kynnt í flýtiflipanum **Útgáfur** á síðunni **Skilgreiningar**.
    2. Bindandi **ConfigurationVersion: String = @. PublicVersionNumber** þýðir að gildi opinberu útgáfunnar af útgáfu hverrar ER-stillingar er tekið úr reitnum **PublicVersionNumber** í töflunni **ERSolutionVersionTable** og komið fyrir í liðnum **ConfigurationVersion**.
    3. Bindandi **ConfigurationTitle: String = @.'>Relations'.Solution.Name** gefur til kynna að nafn ER-stillingar sé tekið úr reitnum **Heiti** í töflunni **ERSolutionTable** sem metur með því að nota mörg-við-ein tengslin (**'>Relations'**) á milli taflanna **ERSolutionVersionTable** og **ERSolutionTable**. Heiti ER-stillinga núverandi forritstilviks eru sett fram í stillingatrénu á síðunni **Skilgreiningar**.
    4. Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** þýðir að heiti skilgreiningaveitunnar sem á núverandi skilgreining er tekið úr reitnum **Heiti** í töflunni **ERVendorTable** sem metur með því að nota mörg-við-ein tengsl á milli taflanna **ERSolutionTable** og **ERVendorTable**. Heiti ER-skilgreiningaveita eru sett fram í stillingatrénu á síðunni **Skilgreiningar** í síðuhaus hverrar skilgreiningar. Finna má allan listann yfir veitendur ER-stillinga á töflusíðunni **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Veitandi skilgreiningar**.

    ![Hönnuðarsíða líkanavörpunar rafrænnar skýrslugerðar, listi yfir bundin atriði gagnalíkans.](./media/GER-JoinDS-Set1Review.PNG)

6. Í skilgreiningartrénu stækkarðu gagnalíkansliðinn **Set1.Summary**:

    1. Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** gefur til kynna að liðurinn **Set1.Summary.VersionsNumber** sé bundinn uppsöfnunarreitnum **VersionsNumber** í gagnagjafanum **VersionsSummary** af gerðinni **GroupBy** sem var skilgreindur til að skila fjölda skráa í töflunni **ERSolutionVersionTable** í gegnum gagnagjafann **Versions**.

    ![Breyta færibreytusíðu „Flokka eftir“.](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. Lokið síðunni.

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a>Skoðaðu vörpun ER-líkans (hluti 2)

Yfirfara stillingar á hlut líkanavörpunar rafrænnar skýrslugerðar. Íhluturinn er stilltur til að fá aðgang að upplýsingum um útgáfur af ER-stillingum, upplýsingum um stillingar og stillingarveitendur með notkun á gagnagjafa af gerðinni **Join**.

1. Í skilgreiningatrénu stækkarðu gagnalíkansliðina **Set2** og **Set2.Details**. Bindingin **Upplýsingar: Færslulisti = Upplýsingar** gefur til kynna **að hluturinn Set2.Details** sé bundinn við gagnagjafann **Upplýsingar** sem er skilgreindur sem gagnagjafi gerðarinnar **Samtenging**.

    ![Hönnunarsíða líkanavörpunar rafrænnar skýrslugerðar sem sýnir útvíkkuð Set2:Record atriði gagnalíkans.](./media/GER-JoinDS-Set2Review.PNG)

    Hægt er að bæta gagnagjafanum **Join** við gagnaheimild með því að velja gagnagjafann **Aðgerðir\Join**:

    ![Hönnuðarsíða líkanavörpunar rafrænnar skýrslugerðar, Join-gagnagjafagerð.](./media/GER-JoinDS-AddJoinDS.PNG)

2. Veldu gagnagjafann **Upplýsingar**.
3. Veldu **Breyta** í glugganum **Gagnagjafar**.
4. Veldu **Breyta join**.
5. Veljið **Sýna upplýsingar**.

    ![Færibreytusíða JOIN-gagnagjafa.](./media/GER-JoinDS-JoinDSEditor.PNG)

    Þessi síða er notuð til að hanna áskildan gagnagjafa **Gerð Join**. Á keyrslutíma mun þessi gagnagjafi stofna einn sameinaðan lista yfir skrár úr gagnagjöfum í hnitanetinu **Sameinaður listi**. Sameining skráa hefst úr gagnagjafanum **ConfigurationProviders** sem er í hnitanetinu sem fyrsta (dálkurinn **Gerð** er auður fyrir það). Skrár yfir alla aðra gagnagjafa verða sameinaðar í kjölfarið við skrár í yfirgagnagjafa miðað við röð þeirra í þessu hnitaneti. Skilgreina verður hvern gagnagjafa samtengingar þar sem gagnagjafa undir markgagnagjafa (`1Versions` -gagnagjafi er faldaður undir `1Configurations` einn; `1Configurations` gagnagjafi er faldaður undir **ConfigurationProviders** einn). Hver stilltur gagnagjafi verður að innihalda skilyrði fyrir sameininguna. Í gagnagjafanum fyrir þetta tiltekna **Join** eru eftirfarandi sameiningar skilgreindar:

    - Hver skrá í gagnagjafanum **ConfigurationProviders** (vísað til í töflunni **ERVendorTable**) er aðeins sameinuð við skrár í **1Configurations** (vísað til í töflunni **ERSolutionTable**) sem eru með sama gildi í reitunum **SolutionVendor** og **RecId**. Gerðin **Innra join** er notuð fyrir þessa sameininngu auk eftirfarandi skilyrða fyrir samsvarandi skrár:

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Hver skrá í gagnagjafanum **1Configuration** (vísað til í töflunni **ERSolutionTable**) er sameinuð við einu skrárnar í **1Versions** (vísað til í töflunni **ERSolutionVersionTable**) sem eru með sama gildi í reitunum **Solution** og **RecId**. Gerðin **Innra join** er notuð fyrir þessa sameininngu auk eftirfarandi skilyrða fyrir samsvarandi skrár:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - Valkosturinn **Framkvæma** er stilltur sem **Fyrirspurn** sem þýðir að þessi gagnagjafi verður framkvæmdur á keyrslutíma á gagnagrunnsstigi sem beint SQL-kall.

    Þegar gögn gagnagjafa eru samtengd er hægt að tilgreina skilyrði samtengingar með því að nota önnur pör af svæðum en svæði sem lýsa núverandi AOT-tengslum á milli þessara tafla. Þessa tegund sameininga er einnig hægt að stilla til að framkvæma á gagnagrunnsstigi.

6. Lokið síðunni.
7. Veldu **Hætta við**.
8. Í skilgreiningartrénu stækkarðu gagnalíkansliðinn **Set2.Summary**:

    - Bindandi **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** gefur til kynna að liðurinn **Set2.Summary.VersionsNumber** sé bundinn uppsöfnunarreitnum **VersionsNumber** í gagnagjafanum **DetailsSummary** af gerðinni **GroupBy** sem var skilgreind til að skila fjölda sameinaðra skráa í gagnagjafann **Details** af gerðinni **Join**.
    - Valkostur staðsetningar **Keyrsla** er skilgreindur sem **Fyrirspurn** sem þýðir að þessi **GroupBy** gagnagjafi er keyrður í keyrslutíma sem beint SQL-kall á gagnagrunnsstigi. Þessi hegðun er möguleg vegna þess að grunngagnagjafinn **Upplýsingar** í gerðinni **Samtenging** er skilgreindur sem keyrður á gagnagrunnsstigi.

    ![Færibreytusíða GROUPBY-gagnagjafa.](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. Lokið síðunni.
10. Veldu **Hætta við**.

### <a name="execute-er-format"></a><a name="executeERformat"></a> Framkvæma ER-snið

1. Fáðu aðgang að Finance eða RCS í annarri lotu vafrans þíns með sömu persónuskilríkjum og fyrirtæki og í fyrstu lotunni.
2. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
3. Stækkaðu skilgreininguna **Model to learn JOIN data sources**.
4. Veldu skilgrieninguna **Format to learn JOIN data sources**.
5. Veljið **Hönnuður**.
6. Veljið **Sýna upplýsingar**.
7. Veldu **Vörpun**.
8. Veldu **Stækka/Minnka**.

    Þetta snið er hannað til að fylla út myndaða textaskrá með nýrri línu fyrir hverja útgáfu skilgreiningar á rafrænni skýrslugerð (**Útgáfuröð**). Hver mynduð lína inniheldur heiti skilgreiningarveitu sem á núverandi skilgreiningu, heiti skilgreiningarinnar og útgáfu skilgreiningarinnar aðskilin með semikommum. Lokalínan í myndaðri skrá mun innihalda fjölda uppgötvaðra útgáfa af ER stillingum (**Yfirlit** röð).

    ![Hönnunarsíða rafræns skýrslugerðarsniðs, sniðsflipi.](./media/GER-JoinDS-FormatReview.PNG)

    Gagnagjafarnir **Gögn** og **Yfirlit** eru notaðir til að fylla út upplýsingar um stillingarútgáfu á myndaðri skrá:

    - Upplýsingar úr gagnalíkaninu **Set1** eru notaðar þegar þú velur gagnagjafann **Nei** fyrir **Val** á keyrslutíma í notandaglugganum þegar ER-snið er notað.
    - Upplýsingar úr gagnalíkaninu **Set2** eru notaðar þegar þú velur gagnagjafann **Já** fyrir **Val** á keyrslutíma í notandaglugganum þegar ER-snið er notað.

    ![Hönnunarsíða rafræns skýrslugerðarsniðs, vörpunarflipi.](./media/GER-JoinDS-FormatMappingReview.PNG)

9. Veljið **Keyra**.
10. Veldu í glugganum **Nei** í reitnum **Nota JOIN gagnagjafa**.
11. Veljið **Í lagi**.
12. Fara yfir myndaðar skrá.

    ![Rafrænar skýrslufæribreytur mynduðu skrá án þess að nota JOIN-gagnagjafa.](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>Greindu framkvæmdarakningu fyrir ER snið

1. Í fyrstu lotu af Finance eða RCS velurðu **Hönnuður**.
2. Veldu **Afkastarakningu**.
3. Í hnitanetinu **Afkastarakningu** velurðu efstu skrána yfir nýjustu framkvæmdarmerki á ER sniði sem notaði núverandi íhlut líkanavörpunar.
4. Veljið **Í lagi**.

    Tölfræði framkvæmdar segir til um tvítekin köll í forritstöflur:

    - **ERSolutionTable** hefur verið kallað eins oft og þú ert með stillingar útgáfu færslur í töflunni **ERSolutionVersionTable**, meðan fjölda slíkra kallana gæti fækkað á tímum til að bæta árangur.
    - **ERVendorTable** hefur verið kallað tvisvar fyrir hverja skilgreiningarútgáfu skráa sem var uppgötvuð í töflunni **ERSolutionVersionTable**, meðan einnig væri hægt að fækka fjölda slíkra kallana.

    ![Tölfræði framkvæmdar á hönnunarsíðu líkanavörpunar rafrænnar skýrslugerðar.](./media/GER-JoinDS-Set1Run2.PNG)

5. Lokið síðunni.

### <a name="execute-er-format"></a> Framkvæma ER-snið

1. Skiptu yfir í flipann á vafranum þínum með seinni lotu Finance eða RCS.
2. Veljið **Keyra**.
3. Veldu í glugganum **Já** í reitnum **Nota JOIN gagnagjafa**.
4. Veljið **Í lagi**.
5. Fara yfir myndaðar skrá.

    ![Rafrænar skýrslufæribreytur mynduðu skrá með því að nota JOIN-gagnagjafa.](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a> Greindu framkvæmdarakningu fyrir ER snið

1. Í fyrstu lotu af Finance eða RCS velurðu **Hönnuður**.
2. Veldu **Afkastarakningu**.
3. Í hnitanetinu **Afkastarakningu** velurðu efstu skrána yfir nýjustu framkvæmdarmerki á ER sniði sem notaði núverandi íhlut líkanavörpunar.
4. Veljið **Í lagi**.

    Tölfræði segir til um eftirfarandi:

    - Gagnasafn forrita hefur verið kallað einu sinni til að fá skrár úr töflunum **ERVendorTable**, **ERSolutionTable** og **ERSolutionVersionTable** til að fá aðgang að áskildum reitum.

    ![Tölfræðiupplýsingar um afköst á hönnunarsíðu líkanavörpunar rafrænnar skýrslugerðar.](./media/GER-JoinDS-Set2Run2.PNG)

    - Forritagagnagrunnur hefur verið kallaður einu sinni til að reikna út fjölda stillingarútgáfa með því að nota sameiningar sem voru stilltar í gagnagjafanum **Upplýsingar**.

    ![Hönnunarsíða líkanavörpunar rafrænnar skýrslugerðar sem sýnir köll í gagnagrunn forrits.](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a>Takmarkanir

Eins og sjá má í dæminu í þessari grein er hægt að smíða gagnagjafann **TENGJAST** úr ýmsum gagnagjöfum sem útskýra hvert gagnasafn færslanna fyrir sig sem þarf að lokum að tengja saman. Hægt er að skilgreina þessa gagnagjafa með því að nota innbyggðu rafrænu skýrslugerðarvirknina [SÍA](er-functions-list-filter.md). Þegar gagnagjafinn er skilgreindur þannig að hann er kallaður fram yfir gagnagjafann **TENGJAST** er hægt að nota fyrirtækjasvið sem hluta af skilyrðinu fyrir gagnavalið. Fyrsta innleiðingin á gagnagjafanum **TENGJAST** styður ekki gagnagjafa af þessari gerð. Til dæmis þegar kallað er á gagnagjafa sem byggir á [SÍU](er-functions-list-filter.md) innan umfangs keyrslunnar á gagnagjafa **TENGJAST**, ef gagnagjafinn sem kallað er á inniheldur fyrirtækjasvið sem hluta af skilyrðinu fyrir gagnavalinu, á undantekning sér stað.

Í Microsoft Dynamics 365 Finance útgáfu 10.0.12 (ágúst 2020) er hægt að nota fyrirtækjasvið sem hluta af skilyrðinu fyrir gagnavali í gagnagjöfum sem byggja á [SÍU](er-functions-list-filter.md) sem er kallað á innan umfangs keyrslunnar á gagnagjafa **TENGJAST**. Vegna takmarkanna á smið [fyrirspurnar](../dev-ref/xpp-library-objects.md#query-object-model) í forritinu eru fyrirtækjasviðin aðeins studd fyrir fyrsta gagnagjafa af gagnagjafanum **TENGJAST**.

### <a name="example"></a>Dæmi

Til dæmis verður þú að kalla einu sinni á gagnagrunn forritsins til að fá listann yfir erlendar viðskiptafærslur margra fyrirtækja og upplýsingar um birgðavöruna sem vísað er til í þessum færslum.

Í slíku tilfelli skilgreinir þú eftirfarandi gervinga í líkanavörpun rafrænu skýrslugerðarinnar:

- **Intrastat** rótargagnagjafinn sem sýnir **Intrastat** töfluna.
- **Vörur** rótargagnagjafinn sem sýnir **InventTable** töfluna.
- **Fyrirtæki** rótargagnagjafinn sem skilar lista yfir fyrirtæki (**DEMF** og **GBSI** í þessu dæmi) þar sem aðgangur að færslunum er nauðsynlegur. Fyrirtækjakóðinn er fáanlegur úr reitnum **Companies.Code**.
- **X1** rótargagnagjafinn sem er með segðina `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))`. Sem hluti af skilyrðinu fyrir gagnaval, inniheldur þessi segð skilgreininguna á fyrirtækjasviðunum `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)`.
- **X2** gagnagjafinn sem faldað atriði gagnagjafans **X1**. Þar á meðal segðina `FILTER (Items, Items.ItemId = X1.ItemId)`.

Að lokum er hægt að skilgreina gagnagjafann **TENGJAST** þar sem **X1** er fyrri gagnagjafinn og **X2** er seinni gagnagjafinn. Hægt er að tilgreina **Fyrirspurn** sem valkostinn **Keyra** til að þvinga rafræna skýrslugerð til að keyra þennan gagnagjafa á gagnagrunnsstigi sem beint SQL-kall.

Þegar skilgreindur gagnagjafi er keyrður á meðan keyrsla rafrænnar skýrslugerðar er [rakin](trace-execution-er-troubleshoot-perf.md) er eftirfarandi yfirlýsing sýnd í hönnuði fyrir líkanavörpun rafrænnar skýrslugerðar sem hluti af afkastarakningu rafrænnar skýrslugerðar.

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> Villa kemur upp ef keyrður er **TENGJAST** gagnagjafi sem hefur verið skilgreindur þannig að hann innihaldi skilyrði gagnavals sem er með fyrirtækjasvið fyrir frekari gagnagjafa af keyrða gagnagjafanum **TENGJAST**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Rekja framkvæmd á sniði rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
